# Ratio: CSP

## On CSP Antoine Mottet (Charles University, Prague) 22 Jan 2021

The CSP complexity does not depend on definable relations, neither relations
definable in the power of the domain

*Partial order* D'<= D if  D' can be obtained from D by interpretaton and
product. Actually it is enough to take one product and one interpretation.

Main Thm of CSP [Bulatov Zhuk]
: If K_3 is not smaller then D then CSP(D) is in PTIME

Def Polymorphism $f:D^n\to D$ of (D,R_1,\dots,D_k)$
We take $n$ colums that are in R, apply f row-wise then the result should be in
R too. 

## Polymorphic principle: 
if $h_1,\dots, h_n: V\to D$ are solutions to an instance of CSP(D) then
$f(h_1,\dots,h_n): V\to D$ is also a solution.

This principle narrows the search space for a solution. This resolves
non-determinism in the search of a solution. 

The set of polymorphisms of a structure contains projections and is closed
under composition.  [clone theory in universal algebra]

Thm: [Barto-Kozik]
TFAE:
* K_3 is not smaller than D
* There exists a polymorphism f s.t $f(x_1,\dots,x_n)=f(x_2,\dots,x_n,x_1)$
And there is a bound on the arity $n$

 Universal theme:
 * symmetric problems can be solved (more) efficiently
 * symmetries are measured by equations
   * He has a paper on unification
   * Mean-payoff games [Atserias]

## Algorithms

### Local consistency methods aka Datalog
Propagate local information
Thm [Larose-Kozik]: For finite D TFAE:
* There is a datalog program pi st X\not\to D iff \pi\sat X
* There are polymorphisms satisfying certain equations

### Linear relaxation
Encode CSP as a system of equations over Q. A variable says how much of every
value we take. Constraints say that you have enough (some consistency
constraints)

The power of these relaxations is completely characterized.

### Gausian elimination
Solutions are generated from a small set using polynomials.

## Infinite domains CSP

Here polymorphisms are not good for characgterisation

D=(N,{0},+1,\Halt) has no K_3 inside but is undeciddable

### CSP over (Z,\leq) 
Relations FO-definable in (Z,\leq) 
We take D=(Z,R_1,\dots,R_k)
Such CSP(D) is either in P or NP-complete
It is also characterizad by existence of max polymorphism in  D.

Thm: MPG is PTIME equivelent to solving CSP(Z,..) [when weights represented in
unary]

Q: How to encode parity games as a CSP problem?

### CSP over (Z,+,1) definable relations
This is characterized

### Open CSP over (Z,+,<) i.e. Presburger arithmetic

### omega-categorical CSP's
 Consider relations FO-definable over a tame structure A
 A structure is omega-categorical if a function counting its orbits does not get
 \infty for any arity
 Then there are more and more tame structures depending on how many orbits are
 needed to cover A^n

 ## Applications to ontology
 


#RATIO

#seminar 22 jan 2021