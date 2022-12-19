---
title: "External Representations in the Age of Large Language Models (LLMs)"
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

https://twitter.com/geoffreylitt/status/1599200960458260482
- Geoffrey got ChatGPT to use debugging/print statements and it seemed to improve perf!

# Humans Are Not Turing Machines

Humans are not Turing Machines.
- finite memory
- error prone
- etc.

Humans plus pencil and paper are Turing Machines.

In fact, in Turing's original description of a Turing machine, he directly calls out the tape as
being analogous to "paper!"

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
> Computing is normally done by writing certain symbols on paper. We
may suppose this paper is divided into squares like a child's arithmetic book.
In elementary arithmetic the two-dimensional character of the paper is
sometimes used. But such a use is always avoidable, and I think that it
will be agreed that the two-dimensional character of paper is no essential
of computation. I assume then that the computation is carried out on
one-dimensional paper, *i.e.* on a tape divided into squares. I shall also
suppose that the number of symbols which may be printed is finite. If we
were to allow an infinity of symbols, then there would be symbols differing
to an arbitrarily small extent.... <!-- The effect of this restriction of the number
of symbols is not very serious. It is always possible to use sequences of
symbols in the place of single symbols. Thus an Arabic numeral such as 17 or 999999999999999 is normally treated as a single symbol. Similarly
in any European language words are treated as single symbols (Chinese,
however, attempts to have an enumerable infinity of symbols). The
differences from our point of view between the single and compound symbols
is that the compound symbols, if they are too lengthy, cannot be observed
at one glance. This is in accordance with experience. We cannot tell at
a glance whether 9999999999999999 and 999999999999999 are the same. -->
>
> The behaviour of the computer at any moment is determined by the
symbols which he is observing, and his "state of mind" at that moment.
We may suppose that there is a bound *B* to the number of symbols or
squares which the computer can observe at one moment. If he wishes to
observe more, he must use successive observations. We will also suppose
that the number of states of mind which need be taken into account is finite.
The reasons for this are of the same character as those which restrict the
number of symbols. If we admitted an infinity of states of mind, some of
them will be "arbitrarily close" and will be confused. Again, the restriction
is not one which seriously affects computation, since the use of more complicated states of mind can be avoided by writing more symbols on the tape.

[(Turing 1936)](https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf)

<!-- He continues to explore a model for human perception of the tape. Specifically that a human can only -->
<!-- perceive some finite number, *L*, of symbols around the current symbol. -->

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

("Consciousness Explained" Daniel C. Dennett 1990. pg 212)

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
> insights of Alan Turing in his observations of his own actions. Dennett (1991) describes the
> context of Turing's discoveries...
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
>
> John Searle's "Chinese room" thought experiment provides a good example of this effect. Imagine a
> room inside of which sits the philosopher Searle. Chinese people come up to the room and push
> strings of Chinese characters through a slot in the door. Searle slips back other strings of
> characters, which the Chinese take to be clever responses to their questions. Now, Searle does not
> understand Chinese. He doesn't know the meaning of any Chinese character. To him, the characters
> of written Chinese are just a bunch of elaborate squiggles. However, Searle has with him in the
> room baskets of Chinese characters, and he has a rulebook which says that if he gets certain
> sequences of characters he should create certain other sequences of characters and slide them out
> the slot.
>
> Searle intends his thought experiment as a demonstration that syntax is not sufficient to produce
> semantics. According to Searle, the room appears to behave as though it understand Chinese; yet
> neither he nor anything in the room can be said to understand Chinese. There are many arguments
> for and against Searle's claims, and I will not review them here. Instead, I want to interpret the
> Chinese room in a completely different way: The Chinese room is a sociocultural cognitive system.
> The really nice thing about it is that it shows us very clearly that the cognitive properties of
> the person in the room are not the same as the cognitive properties of the room as a whole. There
> is John Searle with a basket of Chinese characters and a rulebook. Together he and the characters
> and rulebook in interaction seem to speak Chinese. But Searle himself speaks not a word of Chinese.

("Cognition in the Wild" - Edwin Hutchins pp360-362)

Humans plus pencil and paper are Turing Machines.

So why do we expect LLMs, like GPT, to behave like Turing Machines yet also to approximate human
intelligence? Because they run on computers? Fair, but we can only enhance them if we give models
like GPT access to external representations.

No doubt, LLMs will get better, more accurate, capable of processing longer and longer
conversations. Yet no matter how much better they get, the question of correctness will always
linger. How can I trust this piece of code will run? Is this argument coherent? Are these facts
correct?

I believe we won't be able to answer such questions without external representations. Sure, the
transformer architecture (or at least variations of it) are Turing complete. However, networks
typically don't use their output as a Turing machine tape unless explicitly guided to do so. Moreover, this representation is not sufficient to,
for example, search the internet or use a typechecker or REPL in reasonable space and time.

Many of the more sophisticated uses of LLMs that are emerging are being used in precisely this way,
with the aid of external representations.

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
