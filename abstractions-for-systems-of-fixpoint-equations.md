# Abstractions for systems of fixpoint equations

- [ ] Look at the full version of the paper where there are more explanations.
[/Users/igw/Library/Mobile Documents/com~apple~CloudDocs/Papers/konig-CONCUR2020-full.pdf]

They say that you do not need to compute closure to use their u up-to function.

## Theory of approximations for systems of fixpoint equations
Concrete domain C and abstract A. $\alpha : C\to A$ and $\gamma:A\to C$
The same condition as for the least fixpoints ensures the correctness of the
approximation for the greatest fixpoints. 
 
Completeness property is strong but probably rare.

## An interpretation of up-to techniques
They are mostly used in co-inductive settings.
Sound up to function $\nu (f;u)\leq \nu f$

Sufficient condition, "compatibility" $u\circ f\leq f\circ u$
extensiveness implies completeness.

Q: is it not too restrictive to consider extensive and idempotent functions as
up-to functions. 
When u is not a closure, then they take the least closure above u.

Q: They say that it is not needed to compute the closure above u, one can either
integrate this computation in the fixpoint system because the closure is the
least fixpoint, or do some special step from time to time.

## Interpretation of a game
Use equivalence between a complete lattice and powersets over the basis
elements.
Q: when a complete lattice is not equivalent to powersets over the basis?
The game standard: we check if a basis element is below the solution

## A local algorithm for solving equations
They do reachability games. They say that they can integrate abstractions in
this setting.

