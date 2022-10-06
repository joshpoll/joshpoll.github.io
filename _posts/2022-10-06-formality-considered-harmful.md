---
title: "Formality Considered Harmful"
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

# "Formality Considered Harmful": A Paper I Love

There are some papers that stick in my mind. These are good papers. But there are some papers that when
I tell others about them, they stick in their minds as well. These are great papers. ["Formality
Considered Harmful" by Shipman and
Marshall](https://link.springer.com/content/pdf/10.1023/A:1008716330212.pdf) is a great paper.

Let's dive in!

<!--more-->

<!-- It's easy to say "people are dumb" or "if only they tasted more structured systems, they would
understand," but this paper pushes back on those ideas. The reason why unstructured systems often
win, is that we spend a lot of time working with unstructured data, ideas, and structures. In
fact, our main goal when using knowledge work tools is to develop that structure. A tool that can't
work with the mess is not very useful for getting us out of it. -->

# The Thesis

> In this paper, we describe how creators of systems that support intellectual work like design, writing, or organizing and interpreting information are particularly at risk of expecting too great a level of formality from their users. To understand the effects of imposing or requiring formality, we draw on our own experiences designing and using such systems.

## Difficulties with Interacting with a Formal System

The authors identify four difficulties of working with formal systems.

### Cognitive Overhead

Formalism introduces several types of cognitive overhead:

1. A user must learn the formal language of the system they are using.
2. A user must learn how to translate their goals and tasks into this language.
3. The formal language may introduce incidental complexity -- like naming, linking, and labeling.
   These features are typically necessary to make implicit relationships explicit and precise,
   especially in written formalisms (as opposed to UIs where direct manipulation can remove the need
   for some of this complexity.)

### Tacit Knowledge

Formalizing a concept requires making tacit knowledge explicit. For example, an English sentence
(typically) has a subject and a predicate. Even though I'm pretty familiar with English, this kind
of representation is part of my tacit understanding. If a formal system required me to identify the
subject and predicate of every sentence, that would be a big stumbling block to my ability to write!

In a software context, a formal system that requires a user to write the type of every variable in a
program may require a user to make explicit the tacit data structures they have in their heads.
There are a lot of benefits to doing that! But it can also slow a programmer down, especially when
they may not have even settled on their types yet.

### Enforcing Premature Structure

Knowledge work is messy. Often someone will start with a tacit and informal idea, maybe a vague
solution to a problem or fuzzy idea of a system architecture, and they will *gradually* make this
idea more explicit and
formal.

This process doesn't proceed in just one direction either. We often make mistakes and have to
backtrack, sometimes literally going back to the drawing board. So formal systems that impose formal
structure too early in this process of figuring out an idea are doomed to failure.

Tools like Jupyter notebooks allow users to be messy. They can copy and edit cells to try out
alternatives. They can view concrete data to decide what to do next or what experiment to try.

Once you have a better sense of what your experiment looks like, you can start to convert your messy
notebook to a Python file or a pipeline. (Something that
[LineaPy](https://github.com/LineaLabs/lineapy) aims to help users to do. I worked for them this
summer, in part to further explore these ideas!)

### Different People, Different Tasks: Situational Structure

Some formal systems assume there is a single, canonical formalism, but sometimes structure is
*task-dependent*. For example, there are a billion and one todo-list apps, in part because each one
chooses to support a different set of tasks by imposing its own unique structure.

## Mitigating Problems of Formal Systems

In addition to identifying problems with formal systems, the authors propose several mitigations:

### Identifying the Essentials for Task

This boils down to formalizing only what is necessary and nothing more. All type systems, for
example, make some tradeoffs on what they choose to formalize and what they don't. Performing array
bounds checking statically, for example, is difficult for both humans and computers. Requiring a
human to prove that they never access out-of-bounds memory is a high formal burden.

### Evaluating Cost/Benefit Trade-Offs to Select Features

Rather than choosing a specific cutoff point for a formalism, you can present a user with a series
of tradeoffs where more formalism = more features. For example, if a user spends time creating
styles for their slides in PowerPoint, they can reuse these templates across their presentations.

### Gradual Formalization and Restructuring

Related to the above, it can be useful for a system to delay its request for formalism until the
system actually needs it. In this way, systems like gradual typing can function with only partially
formalized structure. Only when, say, a user wants to do a complicated refactor or document an API
might they consider creating that formalism.

This is especially important because a users' understanding of a problem and its formalization may
change over time. Systems should be flexible to account for this.

### Ephemeral Structure on Demand

Another useful technique is to infer structure, but have that inference change. Thus, rather than
having a static formalism that must be changed explicitly, one can have a rapidly changing formalism
without user intervention. Type inference is one example of this kind of structure. Another form of
ephemeral structure (though not necessarily inferred) is the ephemeral group created when you
multi-select elements in programs like Illustrator. These ephemeral groups can be used to
restructure text or diagrams, but then they disappear once the objects are deselected.

### Training, Facilitating, and Intervention

Finally, while the above were changes to a system, this subsection proposes that a little bit of
training can help users get used to formalisms.

<!-- the authors propose five mitigations:
formalize only the necessary pieces. identifying those can be hard
understand the tradeoffs of adding formal structure vs leaving it out. make some formalisms optional (e.g. you can opt in to heading/body styles in many text editors, but you don’t have to and can instead just style everything yourself)
gradual formalization and restructuring - acknowledge that users’ understandings of their problems changes over time. all for incremental formal structures and mixtures of formal and informal work. suggest ways that the user can formalize something informal
ephemeral structure on demand - infer formal structure, but let it change as the informal structure changes
training, facilitation, intervention - pretty self-explanatory -->

<!-- ## Gradual Formalism

## Inferred Formalism

## Defaults

## Reduce Complexity and Increase Teaching

- gradual formalism: some parts are formal, some parts are not. e.g. gradually building up groups of
  elements when making a diagram
- inferred formalism: automatically infer formal structure from informal specification. e.g. type
  inference. e.g. inferring items are related when they're close together
- defaults: similar to inferred formalism. assume formal structures where they have not been
  specified. e.g. default paragraph style

- reduce the amount of formalism
- train users -->

# Implications

I love formalisms. My research is all about constructing new formal representations of ideas using
programming languages techniques (and right now those ideas happen to be in data visualization).

I remember when [Emery Berger explained that Excel bugs bubbled up to misguided economic
policies](https://www.youtube.com/watch?v=GyWKxFxyyrQ). (Until recently) I've tried to [avoid Jupyter
notebooks](https://www.youtube.com/watch?v=7jiPeIFXb6U) as much as possible. I hate [chasing down
NaNs](https://www.destroyallsoftware.com/talks/wat) in plain JS code.

Yet the popularity of these tools is hard to ignore. Excel is arguably the most popular programming
language (again, thanks to Emery Berger's talk for this). Jupyter notebooks are many scientists'
day-to-day programming interfaces. And JavaScript still rules the web.

While some of this is due to [social
factors](https://lmeyerov.github.io/projects/socioplt/papers/oopsla2013.pdf) beyond the language
itself, there are some shared properties of these tools that seem to influence their adoption, but
may be a hard pill to swallow for the PL-brained
among us.

"Formality Considered Harmful" proposes an explanation for the popularity of these tools. For those of us, like me, who love formalisms,
it can sometimes be hard to see how they can hinder development. But as Meyerovich and Rabkin found
in "Empirical Analysis of Programming Language Adoption," developers value *expressivity* over
*correctness*. This is the tradeoff that many popular tools take, even if it leads to some
grumblings as we use them.

<!-- When we design formal systems it's not sufficient to look at the finished piece of work. When we
analyze a finished program on paper, of course may want to assign types to it and prove its
correctness. When we look at a finished diagram, we may want to describe its structure formally.
While these are useful endeavors, such structures aren't as helpful in the places we spend the most
of our time: with incomplete, inconsistent, nascent formalisms. -->

Furthermore, to understand how we build formal systems that can *really* support users, it's not enough to look at
finished artifacts. These artifacts are dead. Though we can infer some information from a brush stroke, we
gain a whole new perspective by watching a painter in action. The decisions they make, the ideas they
try and revert, the other media they use alongside their paintbrush to hash out ideas.

Hopefully I've convinced you to check out the paper, and maybe think a bit differently when
designing your next formalism.
