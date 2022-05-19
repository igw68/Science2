# Visibility pushdown languages

Nathan Grosshans

He considers AC0 (poly-size, constant depth, unbounded fan-in, with negation)
MOD_m is not definable by those.
ACC0 class with these gates, we do not know that it is not whole NP
TC0: with majority gates instead of MOD_m. It is even stronger class, and we do
not know much about it.
NC1: logorithmic depth, and fan-in 2. 
AC0\incl ACC0\incl TC \incl TC0 \incl NC1

We consider NC1 as the class of efficient parallel log computations.

Thm [Barrington .. Staubing] 
There are regular languages that are NC1-complete under AC0-reductions. 

So if we can separate these classes, then we can separate them with a regular
language.

Thm [Barrington-..-Therien'92]: AC0=FO[<,MOD] for regular languages.

Extending this theorem to bigger classes of languages

Visibly counter languages [Ludwig'18] characterizations of VLCs in AC0. (There
are many problems his thesis).

Main result:
Classification of VPLs into:
- TC0 difficult
- those that are in AC0
- those to which we can reduce MOD_m for all m>=2
- those that are to complicated to prove something about

They hope that their AC0 languages are all what is there.

Ext-algebra: adaptation of forest algebras to visible words

Length-synchronicity
S-> aSb | acSb is not weakly length synchronous
S-> aSb_1 | acSb_2 is length synchronous

Q: what this length sync notion means in terms of trees?

Prop: VPL that is not weakly length-synchronous is TC0-hard
Q: why?









