---
title: "HCI Is the Bottleneck"
excerpt_separator: "<!--more-->"
tags:
  - Uppercase
categories:
  - Blog
---

# HCI Is the Bottleneck in a World with Strong AI

As model capabilities advance, we are rapidly gaining the ability to generate images, videos, and
audio from simple text prompts that are indistinguishable from human-generated content.

Yet, even if we discount existing flaws with models, there's still a huge gap between model
capabilities and systems that are effective in practice. I argue this gap is caused primarily by HCI
problems and not model capabilities, and the gap will only continue to increase as model
capabilities improve.

Is this gap due to failings of HCI? Not entirely. I think it's also due to the mental model of AI
that persists despite growing problems with integrating AI solutions.

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

Improving input and output interfaces is _the_ bottleneck as models get more capable. It can be
viewed as an information-theoretic problem. How do you get more bits of information into the input
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
