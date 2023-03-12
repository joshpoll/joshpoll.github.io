---
title: "Constraint Systems"
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

# Constraint Systems. When Are They Effective?

There's a pattern I've seen many times over: throw it at a global constraint solver.

This invariably does not work because global constraint systems are poorly behaved when they break.
You can't reason about it locally.

Examples:
- SMT
- HM type inference vs. bidirectional typing
- LP solvers and gradient descent for layout
- CAD constraint systems

The other thing is that they often force you to write programs in a particular style that you don't
phrase your domain knowledge in. This is true for e.g. encoding problems as SMT or encoding
diagramming problems in LP.

Good solvers:
- scale linearly with input size
- localize errors well
- provide expressive specification languages

Case Studies:

type inference. HM does not localize errors well. idk about scaling properties (maybe modular
inference for files?). has trouble with more expressive language features. bidirectional typing
ameliorates these problems. the tradeoff is putting more annotation burden on the user

constraint solvers for layout.