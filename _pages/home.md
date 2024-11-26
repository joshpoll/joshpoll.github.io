---
layout: single
permalink: /
title: "Hello!"
classes: wide

# header:
#   overlay_color: "#0C4A6E"
#   overlay_image: /assets/images/mm-home-page-feature.jpg
#   actions:
#     - label: "<i class='fas fa-download'></i> Install now"
#       url: "/docs/quick-start-guide/"
# excerpt: "I'm a fifth year PhD student at MIT. I work on domain-specific languages for graphic representations."
feature_row:
  # - image_path: /assets/images/mm-customizable-feature.png
  #   alt: "customizable"
  - title: "postrational"
    excerpt: "Integrates _formal_ (explicit, technical, abstract) and _intuitive_ (implicit, experiential, concrete) ways of being and doing.  Integrated approaches use direct observation to develop just the right amount of structure, which in turn enhances direct observation."
    # Integrated approaches offer just the right amount of structure to enhance direct observation, which further our exploration of structure.
    # url: "/docs/configuration/"
    # btn_class: "btn--primary"
    # btn_label: "Learn more"
  # - image_path: /assets/images/mm-responsive-feature.png
  #   alt: "fully responsive"
  - title: "interbeing"
    excerpt: "Prefers clusters over categories. Identifies larger spaces or fabrics where clusters live. Rather than seeking to separate phenomena, activities that embody interbeing seek to understand how phenomena are connected. (This term comes from [the Plum Village Buddhist tradition](https://en.wikipedia.org/wiki/Interbeing).)"
    # url: "/docs/layouts/"
    # btn_class: "btn--primary"
    # btn_label: "Learn more"
  # - image_path: /assets/images/mm-free-feature.png
  #   alt: "100% free"
  - title: "aliveness"
    excerpt: 'Promotes authentic self-expression, connection, and joy. Contributes to being fully present and engaged in the world. Dissolves "should"s, fear, and other emotional blockers, constrictions, and hindrances.'
    # url: "/docs/license/"
    # btn_class: "btn--primary"
    # btn_label: "Learn more"
---

I like doing research. My research so far has been in programming languages (PL), human-computer
interaction (HCI), and data visualization (VIS). I especially like building _systems_ that formalize,
clarify, and operationalize research ideas.

The activities that excite me tend to have these three qualities:

{% include feature_row %}

Some of my past and current work includes

<div class="notice--primary">
<b>Key</b>
<br />
<code>*</code> = active
<br />
<code>( )</code> = worked on but not first author
</div>

## Visualization Languages

- \*GoFish: An alive visualization library extending Bluefish
- [\*Bluefish:](https://arxiv.org/pdf/2307.00146) A web-based diagramming library ([bluefishjs.org](https://bluefishjs.org/))
- [Animated Vega-Lite:](https://vis.csail.mit.edu/pubs/animated-vega-lite/) Unifying animation with
  an interactive grammar of graphics

### postrational

Visualization languages aim to construct mappings between data -- formal representations -- and visual
representations, which are perceived intuitively. To what extent can such mappings be
systematized?

### interbeing

How can we view charts, diagrams, notations, and other visual representations as clusters in the
larger space of graphic representations? What shared infrastructure and theory can we build?

How far can we take the _congruence principle_? What happens if we adopt the PL stance that
everything is data (including functions, code, etc.)?

### aliveness

How do we make visualization languages that are truly malleable and expressive? What if a
visualization library optimized for whimsy and character instead of (just) precision, correctness,
and efficiency?

## Accessibility

- \*Mantis: A screen magnification tool
- \*Benthic: A screen reader tool for charts and diagrams
- [(\*Olli):](https://vis.csail.mit.edu/pubs/olli/) An extensible visualization library for screen reader accessibility

### postrational

To what extent can a graphic representation be modeled as a perceptual data structure a la [Larkin & Simon 1987](https://onlinelibrary.wiley.com/doi/pdf/10.1111/j.1551-6708.1987.tb00863.x)?

### interbeing

What can we learn from co-designing visual and accessible representations? Are there meaningful,
visual-agnostic ways to think about visualization? What can we learn about the nature of spaces and
encodings by examining other sensory modalities? What do Gestalt relations look like in other
modalities?

### aliveness

How do we allow more people to enjoy the benefits of visualization? How do we allow more people to
read and write them?

What affordances do modalities besides vision have for external representations? Touch? Sound? How
is information or intent conveyed through these channels?

## Semi-Formal Programming

- [\*Semi-Formal Notebooks:](https://vis.csail.mit.edu/pubs/semi-formal-design-space/) A notebook for semi-formal programming
- Twofish: A direct manipulation editor for Bluefish

### postrational

Until recently, programming languages and environments have only been able to reason about formal
artifacts/representations: types, syntax, semantics, etc. With the invention of foundation models, we can
more easily build general-purpose systems that can leverage intuitive methods. How do we build
systems around those ideas? How do we leverage existing best-practice intuitive methods? When are
they more effective than formal ones? Where do they break down?

### interbeing

How does this expand our notion of what a program is? What if a program wasn't just text but
also contained visual artifacts? What if programs were ambiguous, inconsistent, or otherwise
incomplete, but could still be executed? There's been lots of exciting work in this area, before
foundation models, but now we can actually execute/reason about the "intuitive" parts instead of
just executing/reasoning around them.

### aliveness

How might this allow us to extend the benefits of programming to more people? Code assistants like
GitHub Copilot and Cursor seem to be a qualitative step change in the way we write code. Now it's
possible to write code in a much looser, freer way that's closer to a continuous flow state. Can
we extend this to more people and domains?
