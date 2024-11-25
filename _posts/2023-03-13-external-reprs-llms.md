---
title: "Humans Are Not Turing Machines"
excerpt_separator: "<!--more-->"
tags:
  - Uppercase
categories:
  - Blog
---

One criticism of current LLMs is that they can't reliably do sophisticated math or logic problems
out of the box that humans seem to be capable of. In essence, while humans are Turing-complete,
today's LLMs are not.

But wait... are humans even Turing-complete?

<!-- # Humans Are Not Turing Machines -->

We like to think that humans are great at complex reasoning. But put a person in a blank room with
nothing to write on, and they're getting nowhere fast.

Modern human cognition _depends_ on our abilities to write, diagram, or otherwise externalize thought so that
we can communicate ideas to others, or simply extend our own working memory.

Disclosure: Some of the links below are affiliate links. This means that, at zero cost to you, I
will earn an affiliate commission if you click through the link and finalize a purchase. I wrote
this article without affiliate links in mind.
{: .notice}

<!--

points I want to make in this post:
- humans are not turing machines b/c our short-term/working memory is effectively finite
- humans + pen&paper *are* turing machines. in fact Turing's original model was of this combined system!
- LLMs appear to work better if they are forced to write down their reasoning step-by-step, write
  debug statements, etc.
  - one possible explanation for this behavior is they also need some kind of external
    representation to help them "think"
  - or maybe it's just some sort of priming thing that statistically produces better answers?
  - or maybe it forces them to do easier subproblems?
- in any case, in the short-to-medium term, interfaces between humans and machines, even if those
  machines get more and more "agency," will continue to be central to our communication. That takes
  the form of informal representations like natural language text, art, graphic design, etc. but it also takes the form of
  more precise representations like diagrams, code, proofs, etc.
- In practice, there is no clear boundary between the two kinds of representation (as with many
  things!). Frequently, representations move back and forth between formal and informal. A diagram
  might start out on a whiteboard. A proof might start out as a sketch. And of course there are
  Terry Tao's three stages of mathematical maturity. The friction between these modes generates a
  wonderful fractal turbulence that we can study for a long time to come.
- As deep learning models become more powerful and their outputs more intricate, interfaces for them
  will become even more central and compelling problems, because as the bar for writing/generating
  information continues to lower, the importance of reading/editing information increases.

https://twitter.com/geoffreylitt/status/1599200960458260482
- Geoffrey got ChatGPT to use debugging/print statements and it seemed to improve perf! -->

<!-- When we compare LLMs to humans, we often place a lot of emphasis on how good LLMs are at pure
reasoning. We tend to think that humans are great at sophisticated logic and reasoning. But put a
human in an empty box and ask them to come up with a proof or write a novel, and they will have a
very hard time. -->

<!-- # Humans Are Not Turing Machines -->

<!-- Humans are not Turing Machines. -->
<!-- We tend to think that a Turing Machine is a model of human -->
<!-- cognition, but that's not quite right. If we go back to Turing's original paper, we find that humans -->
<!-- are not Turing Machines, but humans with the aid of pencil and paper are. -->

## Turing Machines

A Turing Machine has the following pieces:

- a tape
- a read/write head for the tape
- a finite state machine that controls the read/write head

But have you ever wondered where this model came from? I had never read the Turing's original paper
until I came across some commentary about it in the conclusion to Edwin Hutchins's book about
distribute cognition: ["Cognition in the Wild."](https://amzn.to/3yzyYWV)

<!-- A Turing Machine has two pieces: a finite state machine and a linear tape. The finite state machine
is a model of the human brain. The linear tape is a model of pencil and paper. -->

<!-- Humans are not Turing Machines.
- finite memory
- error prone
- etc.

Humans plus pencil and paper are Turing Machines.

In fact, in Turing's original description of a Turing machine, he directly calls out the tape as
being analogous to "paper!" -->

<!-- Emphasis mine
> We have said that the computable numbers are those whose decimals
are calculable by finite means. This requires rather more explicit
definition.... **For the present I shall only say that the justification
lies in the fact that the human memory is necessarily limited.**
>
> We may compare a man in the process of computing a real number to a
machine which is only capable of a finite number of conditions q1, q2, ..., qR;
which will be called "*m*-configurations". The machine is supplied with a
"tape" **(the analogue of paper)** running through it, and divided into
sections (called "squares") each capable of bearing a "symbol".
> ... -->

**This is the key takeaway:** Humans are not Turing Machines. Humans paired with pencil and paper are.
{: .notice--info}

Here's what Turing has to say about his original formalism [[Turing 1936]](https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf). He is attempting to formalize the
process by which human computers calculate numbers.

## Tape = Paper

> Computing is normally done by writing certain symbols on paper. We
> may suppose this paper is divided into squares like a child's arithmetic book.
> In elementary arithmetic the two-dimensional character of the paper is
> sometimes used. But such a use is always avoidable, and I think that it
> will be agreed that the two-dimensional character of paper is no essential
> of computation. I assume then that the computation is carried out on
> one-dimensional paper, _i.e._ on a tape divided into squares. I shall also
> suppose that the number of symbols which may be printed is finite. If we
> were to allow an infinity of symbols, then there would be symbols differing
> to an arbitrarily small extent. <!-- The effect of this restriction of the number
> of symbols is not very serious. It is always possible to use sequences of
> symbols in the place of single symbols. Thus an Arabic numeral such as 17 or 999999999999999 is normally treated as a single symbol. Similarly
> in any European language words are treated as single symbols (Chinese,
> however, attempts to have an enumerable infinity of symbols). The
> differences from our point of view between the single and compound symbols
> is that the compound symbols, if they are too lengthy, cannot be observed
> at one glance. This is in accordance with experience. We cannot tell at
> a glance whether 9999999999999999 and 999999999999999 are the same. -->

So the tape in a Turing Machine formalizes the role of paper.

## Read/Write Head = Eyes & Hand+Pencil

> The behaviour of the computer [the person computing!] at any moment is determined by the
> symbols which he is observing, and his "state of mind" at that moment.
> We may suppose that there is a bound _B_ to the number of symbols or
> squares which the computer can observe at one moment. If he wishes to
> observe more, he must use successive observations.

So the read/write head formalizes the eyes and hand+pencil of the person computing numbers.

## Finite State Machine = Human

> We will also suppose
> that the number of states of mind which need be taken into account is finite.
> The reasons for this are of the same character as those which restrict the
> number of symbols. If we admitted an infinity of states of mind, some of
> them will be "arbitrarily close" and will be confused. Again, the restriction
> is not one which seriously affects computation, since the use of more complicated states of mind can
> be avoided by writing more symbols on the tape.

So it is only the _finite state machine_ that formalizes the human themselves.

<!-- He continues to explore a model for human perception of the tape. Specifically that a human can only -->
<!-- perceive some finite number, *L*, of symbols around the current symbol. -->

Daniel C. Dennett summarizes the process Turing seems to have gone through when developing the
Turing Machine in ["Consciousness Explained:"](https://amzn.to/3Teffpl)

> He was thinking, self-consciously and introspectively, about just how he, a mathematician, went
> about solving mathematical problems or performing computations, and he took the important step of
> trying to break down the sequence of his mental acts into their primitive components. "What do I
> do" he must have asked himself, "when I perform a computation?
> Well, first I ask myself which rule applies, and then I apply the rule,
> and then write down the result, and then I look at the result, and then
> I ask myself what to do next, and..." Turing was an extraordinarily
> well-organized thinker, but his stream of consciousness, like yours or
> mine or James Joyce's, was no doubt a variegated jumble of images,
> decisions, hunches, reminders, and so forth, out of which he managed
> to distill the mathematical essence: the bare-bones, minimal sequence
> of operations that could accomplish the goals he accomplished in the
> florid and meandering activities of his conscious mind.

# How Did We Get Here?

Why do we tend to equate humans and Turing Machines? Here's Hutchins's account of it. I don't fully
agree, but it is a decent summary.

> Now, here is what I think happened. It was discovered that it is possible to build machines that
> can manipulate symbols. The computer is nothing more than an automated symbol manipulator. And
> through symbol manipulation one can not only do things we think of as intelligent, like solving
> logical proofs or playing chess; we know for a fact that through symbol manipulation of a certain
> type it is possible to compute any function that can be explicitly specified. So, in principle,
> the computer could be an intelligent system. The mechanical computers conceived by Charles Babbage
> to solve the problem of unreliability in human compilers of mathematical and navigational tables
> were seen by his admirers to have replaced the brain: "The wondrous pulp and fibre of the brain
> had been substituted by brass and iron; [Babbage] had taught wheelwork to think" (H. W. Buxton,
> cited in Swade 1993). Of course, a century later it would be vacuum tubes that created the
> "electronic brain."
>
> But something got lost in this move. The origin myths of cognitive science place the seminal
> insights of Alan Turing in his observations of his own actions....
>
> Originally, the model cognitive system was a person actually doing the manipulation of the symbols
> with his or her hands and eyes. The mathematician or logician was visually and manually
> interacting with a material world. A person is interacting with the symbols and that interaction
> does something computational. This is a case of manual manipulation of symbols.
>
> Notice that when the symbols are in the environment of the human, and the human is manipulating
> the symbols, the cognitive properties of the human are not the same as the properties of the
> system that is made up of the human in interaction with these symbols. The properties of the human
> in interaction with the symbols produce some kind of computation. But that does not mean that that
> computation is happening inside the person's head.

# LangChain, Bing Chat, and the Near Future of LLMs

Humans plus pencil and paper are Turing Machines.

So why do we expect LLMs, like GPT, to both behave like Turing Machines yet also approximate human
intelligence? Because they run on computers? Fair, but (at least right now) we can only grant GPT the
power of Turing-completeness by giving it access to external representations like web search, a
Python REPL, or a database -- the modern equivalents of Turing's pencil and paper.

This is why I'm bullish in the near-term on solutions like Bing chat and
[LangChain](https://langchain.readthedocs.io/en/latest/) that provide such external representations.

No doubt, LLMs will get better, more accurate, capable of processing longer and longer
conversations. Yet no matter how much better they get, the question of correctness will always
linger. How can I trust this piece of code will run? Is this argument consistent? Are these facts
correct?

I believe we won't be able to answer such questions without external representations. Sure, the
transformer architecture (or at least variations of it) is Turing complete [[Pérez et al.
2019]](https://arxiv.org/abs/1901.03429). However, today's networks don't typically use their
outputs as Turing tapes unless explicitly guided to do so (think step-by-step). And today's networks
cannot search the internet or emulate a Python REPL in reasonable time and space.

With formal, external representations we can better understand the "variegated
jumble" of an LLM's "mind" and build much more powerful tools that we can interrogate and maybe even
verify. As Turing showed us back in 1936, it's
just like giving a human some pencil and paper and letting them write. ❏

---

Thanks to [Geoffrey Litt](https://twitter.com/geoffreylitt) for reviewing this post. If you enjoyed
it, you might also like my friend Ajay's account of [our adventure trying to get Bing
chat to recommend Dune.](https://thoughts.intimeand.space/quest/)

<!-- Moreover, this representation is not sufficient to, -->
<!-- for example, search the internet or use a typechecker or REPL in reasonable space and time. -->
<!--
Many of the more sophisticated uses of LLMs that are emerging are being used in precisely this way, -->
<!-- with the aid of external representations. -->

<!-- Likewise, though we can push LLMs to generate things that approach arbitrary computation, we
shouldn't expect them to able to do that alone. Rather we ought to enhance them with external
representations. If we are to get any sort of guarantees about the outputs of these machines, we can
only do so using other kinds of representations than the fuzzy one. This is exactly the same problem
we stumbled into with cognitive science. We think that human minds in a vacuum are capable of
arbitrary computation, but lock someone in a room (even supposing they don't go mad) and they will
not (without extreme effort) be able to reproduce the current body of human knowledge without
writing something down. Complex logical arguments are not possible solely in the head without
risking serious errors or lapses in memory.

Moreover, we've already seen many cases where augmenting LLMs with external representations improve
performance: scratchpads, Google searches, etc. -->
