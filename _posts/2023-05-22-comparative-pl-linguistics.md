---
title: "Natural Semantic Metalanguage: The Other, Other ML"
excerpt_separator: "<!--more-->"
tags:
  - Uppercase
categories:
  - Blog
---

What's the difference between being "happy," "contented," and "pleased?" How would you
explain this difference to someone who doesn't know English? For those of us (like me) who are only
fluent in one language, it might come as a surprise that a seemingly basic feeling like "happy" does not
necessarily have a direct analogue in other languages. Comparing similar emotions in other languages
to "happy" biases our analysis towards English and its cultural peculiarities. Is there a way to
describe culturally specific words like "happy" in a culturally agnostic way? This is what the
Natural Semantic Metalanguage (NSM), pioneered by Anna Wierzbicka, sets out to do.

Just as different cultures have different words
to chop up color space, and slightly different pronunciations of vowels, so too do these languages
have different words for feelings. (And in fact for many other kinds of things!)
In each of these areas, we have the challenge of describing cultural differences in a culturally
agnostic way. For colors, we can use a culturally independent color space such as RGB or HSL. For
vowels we can similarly use vowel space, which is parameterized by the first two or three "formant
frequencies." But language is much trickier. While we can ground color and vowel spaces in physics,
it is not at all obvious that we can ground language in some kind of culturally agnostic "concept space."

The NSM approach has been to collect a base set of semantic "primes," which are universal basic
concepts found in all cultures. Some of these primes are: good, bad; big, small; I, you, someone.
NSM attempts to use a collection of 65 primes to define culturally specific words. Let's look at how
NSM is used to distinguish between "happy," "contented," and "pleased."

First, here are Oxford Languages definitions:

- **Happy:** "feeling or showing pleasure or contentment"
- **Contented:** "happy and at ease"
- **Pleased**: "feeling or showing pleasure and satisfaction, especially at an event or a situation"

Notice how "happy" is defined in terms of two other complex words, "pleasure" and "contentment." The
definitions of "happy" and "contented" are nearly circular! Certainly there is a difference between
these three, and these definitions do seem to capture them, but it is hard to tell exactly what
those differences are, especially if you don't speak the language already. Let's contrast this with
the NSM "explications" of these words:

**Happy**

```
X feels something

sometimes a person thinks something like this:
- something good happened to me
- I wanted this
- I don’t want other things

because of this, this person feels something good
X feels like this
```

**Contented**

```
X feels something

sometimes a person thinks something like this:
- something good is happening to me
- I wanted something like this
- I don’t want other things

because of this, this person feels something good
X feels like this
```

**Pleased**

```
X feels something

sometimes a person thinks something like this:
- something good happened
- I wanted this

because of this, this person feels something good
X feels like this
```

(Explications are from "Defining Emotion Concepts" (Wierzbicka 1992).)

Compared to the Oxford Languages definitions, these ones have much more structure. They can be
diffed. These definitions are also written purely in terms of semantic primes, so (at least in
theory) these definitions are culturally agnostic. Because of their use of parallel structure, it is
easier to distinguish subtleties between these definitions. Compare happy's past tense "something
good happened to me" to contented's present tense "something good _is happening_ to me" to pleased's
"something good happened," which doesn't specify the subject. The first contrast is not present in
the Oxford Languages definitions. The second contrast is implicit in "especially at an event or a situation."

# Motivation for this post

In the winter quarter of my freshman year of undergrad, I learned a lot about language. That quarter
I learned four programming languages. In Dan
Grossman's _Programming Languages_ (PL) class (taught by James Wilcox that quarter) I learned SML
(the other ML),
Ruby, and Racket (with a little bit of Haskell thrown into our final assignment for good measure).
In _The Hardware/Software Interface_ (taught by Luis Ceze that quarter) I learned C. At the same time,
I was taking Katarzyna Dziwirek's _Ways of Meaning_, which covers the diversity of culture through
the lens of language.

In my PL class, we were encouraged to compare and contrast the different languages we were learning,
so it felt natural to apply the NSM framework to those languages, too. I wrote a paper about it, but
this post is long enough...
