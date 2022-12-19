---
published: false
title: "On DSL Design"
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

# What Is a Domain-Specific Language (DSL)?

- some attempt at a definition
- some examples
- doesn't Ras have some notes from his course somewhere?

# Why Is Designing a DSL Different From Other Forms of Design?

- not just selecting a finite collection of things, but actually care about (i) composition and (ii)
  users developing their own abstractions
- DSL design is likely not too much different from general-purpose language design except that DSLs
  can rely on existing abstraction mechanisms like modules/namespaces/interfaces/functions/classes,
  etc. and DSLs worry about similar issues, but in more specific domains and leveraging these
  mechanisms.
- design principles for general-purpose languages are often general enough (different kind of
  general from general-purpose language) to apply to DSLs

# Design Principles

Guy Steele Lineage
- worse is better
- cathedral vs. bazaar
- "growing a language" compromise

HOPL Lineage?
- go look at some of the papers

React et al. Lineage
- Dan Abramov writing
- Cheng Lou and ReasonML/ReScript
- Rich Harris and Svelte
- ClojureScript? Elm?

# How Can We Evaluate a DSL?

classical:
- perf
- proofs
- LoC
- time to complete task

alternatives:
- PLIERS framework
- critical reflections
- psychology

# Do We Really Know Anything?

Clearly we have some hard-won experiences about what works and what doesn't. But at the same time
there is very little empirical basis for how design tradeoffs affect users. e.g. working memory
