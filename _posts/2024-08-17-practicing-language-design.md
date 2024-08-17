---
title: "How Do You Get Good at Programming Language Design?"
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

I get asked a lot in the lab to help people out with API and language design. I wish I had resources
I could point people at to learn better, but I don't. As with most (all?) skills, I know that it
should be some combination of deliberate practice and [developing
awareness](/_posts/2024-08-10-mindfulness-abstraction-design.md). I'm slowly building up design
heuristics/how to attune to features of a domain including
[orthogonality](/_posts/2023-06-01-orthogonality.md) and consistency. But I don't have great advice
for practicing language design over and over again.

Instead I have gotten stuck designing just a few languages. I wonder if I could improve faster by
designing more, smaller languages. Maybe it looks like implementing a lot of tools like Git and JAX
as they've done in the [NY Systems Reading Group](https://notes.ekzhang.com/events/nysrg)? Maybe it
looks like implementing various lambda calculi? Building Git and JAX seem to large, getting into the
nitty gritty details not just the core abstraction design. But building
lambda calculi feels both too small and too general purpose for learning DSL design.

Maybe it's useful to distinguish between general-purpose languages and domain-specific ones. General
purpose languages include things like reactive programming languages. Their primitives aren't
specific to any particular task, but instead provide an approach to computation. Differentiable
programming would also fall into this category. So would build systems. On the other hand, maybe a
system like Git or JAX is more domain-specific. They are built on general-purpose ideas like build
systems and auto-differentiation, but include more domain-specific concepts too.

idk