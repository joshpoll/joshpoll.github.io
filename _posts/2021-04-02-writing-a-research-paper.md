---
title: "Writing a Research Paper: A Meta-Guide"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---

**These notes are a work in progress!**
{: .notice--warning}

Writing is not something that has come easily to me. Through middle and high school I routinely
would not complete essays I needed to write for class.

I noticed a big change after I started doing research. After a couple of years of reading and
writing papers and absorbing advice on how to do so, I noticed that both my research writing and
my essay writing dramatically improved. I found it much easier to write.

I still struggle with writing and finishing pieces, but it's much better than it used to be.

In this post I'll provide some scaffolding for many of the resources I have used when writing papers
thus far. I hope to provide a structured collection of resources that both provide a coherent
philosophy on the role of papers in (computer science) academia and actionable tips for improving
the effectiveness of your own work.

<!--more-->

I am acutely aware that I am not in a real position of authority to be offering advice to anyone on
writing. Luckily, you don't have to take my word for it. I have provided copius links to other people
with decades more experience than me.

# Community

What is research about? This lecture from UChicago helped establish my point of view.

Research is about community. See this lecture: [The Craft of Writing Effectively](https://www.youtube.com/watch?v=vtIzMaLkCaM)
{: .notice--primary}

Fundamentally, research is about a *community* of people. From this framing, a research paper is an
argument aimed at *changing the minds* of that community. The rest of this post will be framed with
this perspective in mind. It justifies many other points to come.

# Know Your Audience

Since a paper is designed to convince people of something, it's important to understand who those
people are.

## *Why* are they reading your paper?

- reading group
- literature review
- related work
- ideas for their own work
- just interesting

## *How* are they reading your paper?

- [How to Read a Paper](https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf)
- [How to (seriously) read a scientific paper](https://www.sciencemag.org/careers/2016/03/how-seriously-read-scientific-paper)


- What does your audience already know or believe?
- What does your audience not already know or believe?
- What forms of evidence might convince your audience?

- why do people read papers?
- how do they read them?
- who are you writing for, specifically, and why?
- what things do they know or believe?
- what things do they not know or believe?
- what things might *convince* them?
- speaking their language

**Write papers that are *easy* to read!**
{: .notice--primary}

# Story

- example-driven
- beginning, middle, end
- *one* key message
- conflict-resolution

narrative arc
- exposition, rising action, climax, falling action, resolution
- rising action = problem
- climax = key idea
- falling action = consequences

# The Research Paper Story Archetype

Let's look at how the narrative arc typically plays out in academic papers.

Two related story archetypes:
- Question-Answer: Construct a research question and find an answer.
- Problem-Solution: Identify a problem and construct a solution.

Seems to me that problem-solution is possible as "research" in CS, because systems *embody ideas.*
Systems are formal representations of ideas.
TODO: honestly this probably does exist in other areas, e.g. development of biomedical techniques.

This dichotomy is overly simplistic. Many papers lie somewhere in between these two extremes;
however, research communities often lean to one end or the other. TODO: this claim is a bit weak.
Really need to flesh out this part!

everything else revolves around this central point

- summary: title, abstract, intro
- auxiliary artifacts: twitter, blog, talk, etc.
- context: background, related work
- broader impact: discussion, future work

it's non-fiction! you don't have to stick to prose style. **use structure to your advantage!**

Some notes on how to write research papers in CS (skewed towards PL):
- [SPJ's "How to Write a Great Research Paper"](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/
)
- [Kayvon Fatahalian's "What Makes a (Graphics) Systems Paper
  Beautiful"](http://graphics.stanford.edu/~kayvonf/notes/systemspaper/)
- [Derek Dreyer's "How to Write Papers So People Can Read Them"](https://www.youtube.com/watch?v=XpgJ31GKPWI)

Some great writers/presenters (typically correlated) who you should probably check out (mostly in PL) (alphabetical by last name):
- Emery Berger
- Derek Dreyer
- Jana Dunfield
- Ron Garcia
- Dan Grossman
- Philip Guo
- SPJ
- Shriram Krishnamurthi
- Conor McBride

# Paper Summaries *In Situ*

- Title
- Abstract
- Intro

These are (i) affordances to readers to help them understand your paper and (ii) *in situ* sales
pitches for your paper. Use them effectively!

## Title

## Abstract

The most important part of the abstract is the conflict-resolution pair. Get as quickly as possible
to the conflict, as quickly as possible to the solution, and as quickly as possible to the consequences.

## Intro

The introduction should provide a short, but complete summary of the entire paper. Its structure
should mirror that of the paper such that you can put inline forward references to later parts of
the paper in the proper order. You can go into more detail about the consequences of and evidence
for your resolution here than in the abstract.

# A Spectrum of Evidence

There are far too many types of evidence to mention in one place here, but I will nonetheless point
you at some links to get started.

- [Code and Contribution in Interactive Systems
  Research](https://homes.cs.washington.edu/~jfogarty/publications/workshop-chi2017-codeandcontribution.pdf)
- [CMU Empirical Methods slides](TODO!!!!)
- [Eunice's slides?](TODO!!!!)

The important point for this post is that methods vary not only by the topic and idea you are
writing about, *but also by community.* Different communities value different types of evidence. For
example, POPL is generally interested in formal proofs (where applicable), whereas CHI is interested
in user studies (again, where applicable). There are notable exceptions to these, and they should
not be treated as hard and fast rules. Just remember: evidence must convince a community. That means
they may be looking for statistically rigorous methodology or a description of your research
process, etc.

# Selling Your Paper!

If a paper falls in a forest...

A research paper does little to impact a community if no one in that community reads it! Thus we
must "sell" our papers. We've already seen that portions of the paper can help sell it. But there
are auxiliary artifacts as well. This can be done by
- tweeting about it
- giving a talk
- writing an article
- writing a blog post

Some resources on how to give talks (note: significant overlap with paper writing techniques and
vice versa, so use
those, too!)
- ["How to Give a Great Research
  Talk"](https://www.microsoft.com/en-us/research/academic-program/give-great-research-talk/) - SPJ
- ["How to Design Talks"](https://www.youtube.com/watch?v=aFT79TmffPk) - Ranjit Jhala
- ["Tips for Giving Clear Talks"](http://graphics.stanford.edu/~kayvonf/misc/cleartalktips.pdf) - Kayvon Fatahalian
- ["How to Write a Paper and Give Talks That People Can
  Follow"](https://www.youtube.com/watch?v=ZmFXMREURBI) - Derek Dreyer

# How to Write: Nuts and Bolts

- two styles of writing: full text beginning-to-end vs. outline first

**Draft *then* edit!** Write first, edit second! It's important to separate them into separate phases. This is a technique that can be difficult to internalize but is tremendously
useful not only for writing, but also for most (if not all) creative activities.
{: .notice--primary}

For general tips on writing nonfiction, consider *On Writing Well* by William Zinsser. This is my
dad's go-to book for writing tips.

For a more systematic approach to writing clearly, try *Style: Lessons in Clarity and Grace* by
Joseph M. Williams and Joseph Bizup. This is my undergrad advisor's go-to book for writing tips.

For your really low-level style points, try *The Chicago Manual of Style*. My parents, who are
editors, swear by this book.

## LaTeX

Just learn it.
["Learn LaTeX in 30 Minutes"](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes) - Overleaf

# Wrapping Up

- **community**
- the paper is a medium for convincing people in the community, everything else falls out of that
  principle

## Related Guides

See Philip Guo's ["How to write a good HCI research paper (tips from senior colleagues)"
](https://web.archive.org/web/20210402170523/https://pg.ucsd.edu/how-to-write-hci-research-paper.htm)