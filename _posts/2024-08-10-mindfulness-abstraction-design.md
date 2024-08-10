---
title: "Mindfulness and Abstraction Design"
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

## Formalism and Awareness

Skill building helps us focus our awareness. Formalism is an incredible scalpel for sharpening
thought. It forces us to be really precise about what we mean. There is nothing more formal than a
(classical) computer program. It is even more formal than mathematics.

Formalisms often force us to erase syntactic differences between concepts to uncover more parallels.
A sequence of items is "really" a function from the natural numbers to some items. It's not a
fundamental concept, but one that can be defined in terms of other concepts.

## Abstractions and Interbeing

Many of the most powerful ideas in PL are secretly interbeing concepts. They get rid of previously
rigid boundaries between ideas

- functions are values (functional programming)
- code is data (Lisp)
- types are terms (dependent type theory)

These ideas are often extremely valuable and insightful. They are often both simpler and more
expressive than theories with rigid boundaries. If you have rigid categories, the way to make your
theory more expressive is to add more categories and more categories and more categories and... But
the tradeoff is that theories which conceptually unify ideas can be more confusing since these
boundaries don't exist. They also tend to have recursive definitions all over the place.
Disjoint, non-recursive categories are easier to hold in our minds, even if they are less powerful.

The same pattern of interbeing shows up in data visualization when you interrogate the field formally, but we are just beginning to understand this.

- interaction and animation are both data-driven but differ in the source of that data (user or
  system) [(Animated Vega-Lite)](https://vis.csail.mit.edu/pubs/animated-vega-lite/)
- UIs are diagrams [(Bluefish)](https://vis.csail.mit.edu/pubs/bluefish/)
- text and diagrams exist on a spectrum [(Visual Thinking in Action)](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/Walny2011InfoVis.pdf)
- charts are a special kind of graphic representation (???)