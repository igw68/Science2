# Abstract interpretation of Python programs

#seminar 2022-02-16
Raphael Monat

Analysis of tax code (Prosecco)
Dynamic programming languages:
- object oriented
- dynamic typing (type of a variable may change during an execution)
- Introspection operators: program flow depends on the current type of the object

Semantics is defined by a reference implementation (interpreter)
They have a semantics (that is not executable)
Q: what is their form? Is this operational semantics?     

They do not support recursive functions nor eval.
But the rest of the language is there.

He needs different domains for abstractions.
He uses auxiliary variables to state invariants.

Their approach is to rewrite a language to a core language.

Nice comparison with existing work. He can treat more programs and faster.
It looks like this is very performant wrt to other methods.

Q: what makes it more powerful than the other methods?
Is this due to numeric analyses not present there?

Analysis Python/C at the same time
They have conversions between abstractions for Python and C.

Future works:
- execute their semantics
- improve scalability: incremental, compositional, variable packing

Clever rewritings that are modular and loose less informations.
