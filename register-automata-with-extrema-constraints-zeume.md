# Register automata with extrema constraints, Zeume

Register Automata with Extrema Constraints, and an Application to Two-Variable
Logic. Szymon Torunczyk and Thomas Zeume

FO^2 has a finite model property.
Undecidable with 3 linear orders, but decidable with 1 linear order
**Here they show that with 2 linear orders the logic is decidable.**

With two orders drawn on the plane a model can be seen as a data word. Here we
only look at orders of type \omega.
 
He converts to a Scott normal form: every formula can be converted to a Scott
formula that is equisatisfiable (but not necessarily equivalent)
Q: can we get automaton recognizing exactly the models of the formula?

Automata model: registers, values can be compared wrt to order.

The infinite word case requires supremum and infinimum constraints. (if you go
to order types >\omega)

For horizontal order they can embed any order in rational order.
They will encode it into a tree. Now it is more difficult to say what is to the
right. 

So now a register can store a supremum for all nodes to the right of it (right
in the tree sense).

## Tree register automata with sup and inf constraints
They work on infinite trees. 
They have a parity condition on states
For every register r they have a special registers r_{sup} and r_{inf}
The idea is that auxiliary registers should store sup of all the values of r
below the node. 
Run is accepting if these values of r_{sup}, r_{inf} are always correct, and
each branch sat the parity condition.
Actually values are real numbers

These automata are sufficient to translate FO^2 formulas to it (equisatisfiable)

The emptiness of these automata can be converted to conventional tree register
automata, that are easy to decide.

How to remove auxiliary registers? 


#seminar 30 mar 2021
