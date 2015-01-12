---
layout:     post
title:      Ignoramus et Ignorabimus
date:       2015-01-12 12:00:00
summary:    TODO
categories: research
---

I've been thinking about logic and incompleteness, prompted by the excellent graphic novel Logicomix,
and I came to an interesting realization.

> Some statements are **so** undecidable, proving their undecidability is **also** undecidable.

Full disclosure: I haven't yet worked through the details of the proof, so I might well be wrong.
I also don't know if this is already a well-known fact among logicians, it might be nothing new.
Still, I thought it was an interesting enough insight to be worth writing about, so here goes.

But first, a short primer on incompleteness.


### Incompleteness

One thing I really enjoyed about Logicomix,
was how well it set the mood for what was going on in the mathematical community in Russell's heyday.
The hope of mathematicians at the time was that they could agree on a handful of *axioms*,
and by using only those axioms, prove or disprove any mathematical statement. 
Hilbert, a prominent and formidable mathematician,
captured this sentiment with the slogan
"Wir müssen wissen — wir werden wissen!" (We must know — we will know!).

Logic, it turns out, is not so generous.

Gödel demonstrated the problem in his first incompleteness theorem.
You can pick any handful of axioms you want,
and you still won't be able to realize the goal of proving everything.
If your system of logic is powerful enough to make statements about natural numbers (0,1,2,etc.),
then it is also powerful enough to construct tricky self-referencing statements.
"This statement has no proof".
As a result, logic will always have either
  inconsistencies -- false statements that we can prove to be true (oops)
or
  *undecidable statements* -- statements we can't prove or disprove.

Ignoramus et ignorabimus (we do not know and will not know).


### Open Problems

I remember the first time I learned about Gödel's incompleteness theorems, when I was an undergraduate.
I found the result both fascinating, and thoroughly disappointing.
It seemed wrong that mathematics could be... negotiable.
Could it really be that some mathematical statements are matters of *opinion?*

There was still some hope in my mind, though, that Hilbert was basically right.
We might not be able to prove or disprove everything,
but surely we could at least detect when a problem fell outside the scope of our axioms.

Today, I am convinced of the opposite.
I now think that there are problems so shrouded in mist,
we may never even be able to fully convince ourselves that we can't prove them.
Maybe this is why there are open problems in mathematics.


### Proof Sketch

What want to show is there are some statements that are undecidably undecidable.
That there are some true statements that look like "**'X is undecidable'** is undecidable".

For convenience, let's have S stand for the statement "**'X is undecidable'** is undecidable".
What can we say in general about all such statements?
For starters, if S is true, then X clearly must be undecidable.
(I'm a little suspicious of my own use of the word "clearly," but let's go with it for now and see where it takes us).
If that weren't the case, then "X is undecidable" would be false, so our S would be false as well.

What about if S is false? One of two things must be the case: either "X is undecidable" can be proven true, or "X is undecidable" can be proven false.

All we have to do to finish the proof is pick the right thing for X.
How about X equals "X is undecidable OR U" (where U is some statement known to be undecidable).
 
 - If we can prove "X is undecidable", then we have also proven X true!
   If our logic is to be sound, this **must not** be the case.
 - If we can refute "X is undecidable", we also run into trouble.
   Remember that X stands for "X is undecidable OR U", so if "X is undecidable" is false, then X *is* undecidable. Another contradiction.

What this means is that for this choice of X, S can't be false.
It might be provably true, or it might be itself undecidable,
but it can't be false without causing a contradiction.