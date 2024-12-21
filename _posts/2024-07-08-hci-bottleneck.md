---
title: "HCI Is the Bottleneck"
excerpt_separator: "<!--more-->"
tags:
  - Uppercase
categories:
  - Blog
---

(updated 2024-12-21)

# HCI Is the Bottleneck in a World with Strong AI

As model capabilities advance, we are rapidly gaining the ability to generate images, videos, and
audio from simple text prompts that are indistinguishable from human-generated content.

Yet, even if we discount existing flaws with models, there's still a huge gap between model
capabilities and systems that are effective in practice. I argue this gap is caused primarily by HCI
problems and not model capabilities, and the gap will only continue to increase as model
capabilities improve.

**HCI** stands for Human-Computer Interaction. It refers both to a research discipline and a set of
techniques for designing interactive systems. For the purposes of this post, I am referring to our
theories, practices, and understandings of how to build software interfaces between humans
and computers.
{: .notice--info}

## The Congruence Principle

I come from a visualization-centered HCI background. At the heart of that field is the _congruence
principle_, which states that data and a visual representation of that data should be
isomorphic, or congruent. Some simple examples are mapping every row in a table to a bar in a bar
chart or mapping a binary tree data structure to a node-link tree diagram. But a user interface can
be viewed as a visualization of some underlying computational data structure, too. The spatial
organization, nesting, colors, etc of that interface reflect the underlying data structure.

The challenge I see with building interfaces for AI systems is that they
introduce fundamentally new kinds of computational data and ways of representing them. Latent
spaces, chain-of-thought reasoning, neural circuits, etc. Many of these data structures are way less
formal than existing kinds of data we deal with. They can capture "vibes" and high-level concepts,
not just formal data structures.

AI systems also create much larger, more complex
versions of existing kinds of data. Very large text or code diffs, for example. And with reasoning
models, we need to build interfaces that can handle very long latencies. (Again, lots of precedence
for this. We have long-running computations in notebooks. Lots of human-human communication is
async.)

We don't have great ways of building interfaces for these new kinds of data yet. But lots of people
are trying!

## Benchmarks Are Not Enough

Is this gap due solely to limitations of our understanding of interface design? Not entirely. I
think it's also due to the mental model of AI that persists despite growing problems with
integrating AI solutions.

AI is typically thought of in the following way:

input -> model -> output

The goal of core machine learning is to create the model that optimizes the output given the input,
e.g., producing an output image that most faithfully represents an input text prompt. The central
limitation of this model is that it ignores where inputs come from and where outputs go to. The
picture looks a little more like this:

human -input-> model -output-> human

Even if we assume a perfect model that optimizes the input-output correlation, the model is still
fundamentally limited by the information contained in the input, and the usefulness of the output is
still fundamentally limited by a human's ability to interpret and use it.

As a result, we see rapid progress on the most well-defined problems. Programming and math are probably the
most formal disciplines. And competitions and tests are intentionally designed to have unambiguous
specifications. While some problems we care about might have this form, and probably many problems
we care about have well-defined subproblems, I think most problems we care about underspecified.

Bringing shape to a problem requires back-and-forth communication between humans and AI models. And
so improving input and output interfaces is _the_ bottleneck as models get more capable. We can vie
this as an information-theoretic problem. How do you get more bits of information into the input
stream? How do you allow humans to interpret more bits of information from the output stream? Now,
solutions to these problems aren't simply algorithmic, but also require existing context to
understand. That is, it's not as simple as cramming in more information, but also in doing so in a
way that allows humans to create and understand that information.

## What's the role of HCI with imperfect models?

HCI still has a profound role, possibly a more important role, even with imperfect models. We can think of an imperfect model as a
perfect model with some additional (possibly/probably biased) noise. The HCI problems with imperfect
models are thus the same as with perfect models but with the added difficultly of allowing humans to
understand and handle "noise" in the model output.

## Won't strong AI solve the HCI problem?

Even as models get better at producing interfaces, their capabilities are still limited to the
human<->model feedback loop. This loop can probably be used to design these interfaces (and this is
already starting to happen with things like Copilot and Figma AI, for example), but it doesn't let
us sidestep this problem completely.

## Aren't' UIs just going to be ephemerally generated all the time?

Complex interfaces like the Blenders and Photoshops of the world are still likely to be
semi-stable interfaces rather than ones that are generated on the fly, because of how difficult it
is to learn such interfaces and the benefits humans have when using tools they have deep
knowledge/skill/practice/craft around. So these interfaces are still subject to the feedback loop
problem.

## How do we improve input and output fidelity?

I think I'll save this for another time.
