# Implicit automata and transducers

Thesis of Dung Nguyen

## Basic definitions
- Sequential transducer: output a string on every transition and on final state. 
- Sequential function: function realized by a sequential transducer
- Sequential transducer is aperiodic when its transition monoid is aperiodic

Thm [Krohn-Rhodes]: Every sequential funcition is a composition of aperiodic
sequential transducers with two states and group transducers.

### STT
- Copyfull SST: There are registers, and they can be duplicated in assignments. 
  Definition in the thesis is absurdly formalistic. 
- Copyless SST: every register can be used at most once in register assignment
  on a transition. 
- Regular functions: those defined by copyless STT. This is motivated by many
  other characterizations. 
- Prop 2.3.9 copyless STT need states.
- Prop 2.3.12 Every regular function has a linear bound on its output length.

- Layered SST There is a hierarchy  of registers and copying should respect the hierarchy.
- Thm [DFG20] k-layered SST compute exactly those copyfull SST functions that have growth
  bounded by O(|w|^{k+1}). 

### Polyregular functions
- the smallest class closed under composition and  containing regular functions
  and squaring with underlining. [Boj18]
- Polyregular functions have polynomially bounded output
- Prop 2.5.4 Every function computed by a layered SST is polyregular.
- Prop 2.5.5 Layered SST are those functions that are both poly-regular and HDT0L
- Polyregular functions can be obtained as compositions of single-state
  1-layered SSTs

**The last two propositions show that layered SST are not a good class for
this thesis as their closure under composition are all polyregular functions**

**Q1**: There is a characterization of polyregular functions with polynomial list
functions. Why this is not the last word on characterizing this class with the
lambda-calculus?


## 3. Comparison-free polyregular functions

**Def** Starting with regular functions and applying composition by
substitution.

*Q*: What is the intuition behind taking composition by subsitution as a basic
operation?

There is a variant of squaring with underlining that is cfp. The difference is
that it does not allow to point exactly at the position in the string, but just
copies consequtive letters in front of each copy. 

Prop 3.1.7. Actually CbS operation can take always a regular function as the
first argument. So cfp functions of *rank k* are $CbS(f,(g_i)_{i\in I})$ for $g_i$
of rank k-1.

- Prop 3.1.8 rank k is closed under concatenation and glueing over regular domain

- k-CFPT are machines with stack like peble management. 
  - The main point is that with push the new pebble is put at the first position,
    and not at the current position. Moreover there is no way to  compare
    different positions on the stack.
- (k+1)-CFPTs are   comparison-free polyregular functions of level k. 

**Thm 3.1** [Main] The following are equivalent:
- f is cfp of rank k
- f is cfp and $|f(w)|=O(|w|^{k+1})$
- f can be decomposed as a regular function and cfsquaring.

**Thm 3.2** if f is cfp of rank k then it can be presented as g o cfpow^{k+1}.
This is similar to what happens in pushdown hierarchy. Does this happen too in
polyregular functions, where cfsquaring is replaced by the standard one?

**Thm 3.3** [important] Closure of cfp under composition.

**Thm 3.4.2** Characterization what unary functions are poly-regular (unary input
alphabet)

This characterization is used to get separation results in section 3.5

Thm 3.5.1 cfp functions that are not  HDT0L.
Thm 3.5.2 HDT0L functions that are not cfp.

## 4. Streaming transducers categorically.
Stop before section 4.6

C-SST is as a standard one but R instead of a set of registers is an object in C.
Transition function says how to change state and gives also g:R->R.
A word w generates a function obtained by a composition of g_i's. 
We prefix this function with $i:\bot\to R$, and $o_q:R \to \top$. 
We get a function from \top to \bot. 
Finally, there is a meaning function associating to the every function from \top
to \bot an element in X.

Single state C-SST are very close to C-automata of Colcombet and Pterisan[CP20]

Actually, every C-SST is equivalent to single state SST over some different
category.

Lemma 4.8 An existence of a morphism from streaming setting C to a streaming
setting D shows that C is subsumed by D.

A category of register transitions SR(\Gamma). Composing two register transitions as in
SST. Copylessness is ensured by an additional constraint.

GR(\Gamma) is the copyless setting where \top=\emptyset \bot=unit

Coproduct completion: finite lists of elements of the category.

*State dependent memory SST*. A generalization of copyless SST. 
The idea is that instead of one register set R we have C_q for each control
state.
They are useful for different constructions, still they do not add experssive
power. 
Lemma 4.3.12: state dependent memory SST are the same as one state standard SST.
in terms of expressinveness

### Some function space in SRoplus
On objects in the image of i_oplus there is a function space. 

### Finite product completion 
This is needed if we want function spaces also on other objects.
This gives nondeterministic SSTs. But as in [AD11] nondeterministic SSTs
can be determinized.

**Thm 4.4.7** A variant of [AD11]. Every non-deterministic state-dependent
copyless SST can be uniforminized.
This is easy by fixing a total order on possible morphisms that appear as
transformations.

### Coproduct and product completion
These are double lists: sums of products
Apparently it is very important that SR\with\oplus is monoidal closed (Corollary
4.5.4)
This is a purely category theory result about completions.
This opens a way to do things with lambda-calculus.

### Summary of equivalences
Single-state GR_{\oplus\with}-SST=sdm-GR_\with-SST=
=sdm-GR_SST=regular functions

(sdm = State Dependend Memory)

## Linear \l-calculus
There is some notion of normal form that cannot be \beta-normal form because of
\otimes and \oplus. He needs to allow for some \eta conversions that unlock new
\beta-redexes.
He uses this to understand what are normal forms in Str_\Gamma[\tau] and in
\Tree_\Gamma[\tau]. 

A type is *purely linear* if it does not use ->. 
A term is *purely linear* if it has a derivation using only purely linear types.

### Encoding of strings and trees.
He uses a more precise encoding than Church encoding. 
This is encoding of [Girard87] in \l^{\with\oplus}
Here every letter is interpreted as 0 -o 0 instead of 0->0. 
Similarly for trees. 
Prop 5.1.7: There is a bijection between trees and normal forms in a given type.
That there is nothing else is a conseqeunce of normalisation. 
This is essential for the correspondance. 

Definability [Def 5.1.9] He uses linear implication which means that the
transducer does a single pass. He will later investigate what happens in the
case of strings when he takes normal arrow.

Rem 5.1.14: other variants of the notion of definability (kappa not linear,
different Church encoding), make perfect sense but are not explored in this
thesis.

On strings he also considers definability with normal non-linear arrow not only linear arrow.

#### Regularity is \lambda definability with -o
- Define a syntactic category of linear types and terms between these types
  using some fixed env \G for letters
- This gives a streaming setting \Ell.
- This streaming setting \Ell is initial among all reasonable streaming settings.

- First observation is that \Ell-STT computable functions are exactly
  \l-definable functions. 
  left-to-right is by programming transducer in a term
  right-to-left is by understanding the shape of normal forms in string function
  types. This gives exactly the transducer. So the understanding of normal forms
  is central to this work. 

- Every single state \Ell-SST computes a regular function. 
  First (&4.5.2) single state GR\oplus\with-SST compute regular functions.
  Now since \Ell setting is initial it cannot compute more.

- Every regular function is computed by  \Ell-SST
  He shows a morphism of streaming settings GR -> \Ell
  One simple way would be to encode copyless SST in \l-terms. What he does is
  much more abstract.


#### Comparison-free polyregularity is definability with ->
- Every cfp-function is \l-definable because every regular function is, and
  composition by substitution is programmable in the calculus. The regular
  function statement is from the previous section. 

- Every \l-definable function is cfp.

- Syntactic bureaucracy (section 5.4) is very rough (without explanations)

## Regular tree functions
- A tree streaming setting is similar, but with monoidal product \otimes.

- C-BRTT bottom up go over the tree and label each node iwth a function on R (of
  appropriate arity). The labelling depends on states. So at the end we have a
  value in R for the tree and this value is transated by o function to the
  output in \bot type.

  - Thm 6.1.6 We can reduce to singe state if we work with C_\oplus

- Lemma 6.4.12 TR-one-hole-\with-BRTT compute exactly the regular functions.
  
- Section 6.5 Monoidal closed category TR_{\oplus\with}.

- \l-definable tree functions are regular
  Define \Ell settting then \Ell-BRTT are exactly \l-definable.
  Show that there is a morhism from TR-setting to \Ell-setting
  Then thre is a morphism from TR_{\oplus\with} to \Ell
  The converse is a suitable adaptation of initality result (Lemma 5.2.6 that is
  not proved)

## Star-free languages via non-commutive lambda
I do not understand anything.

# Summary
- This thesis certainly pushed me outside of my confort zone.
- Gives characterizations of what certain \l-calculi can compute
- The abstract setting, with a notion of Streaming setting and morphisms between
  such settings.
- Makes a precise connection between copyless in transducer setting and linear types.
- Remarkable theorem of Hillebrand and Kanellakis'96: A language can be defined
  by a simply typed \l-term using Church encoded strings iff it is regular.
  Here it is very important to allow Str[\tau]-> Bool as functions. 
  Without type subtitutions terms of type \Nat-> \Nat define conditional
  polynomials [Schwichtenber'75]. With substitutions arbitrary tower of
  exponentials is possible. 
  - The proof in one direction is to encode automaton as a lambda-term. 
  - In the other direction Str[tau] has a monoid structure given by composition,
    that is the same as concatenation on strings. Then L={\phi^{-1}(x) : [t](x)=\true}
    the inverse image of a finite set.
- Since a Hom(X,X) has a monoid structure various automata behaviours can be
  described by this monoid.
  - power of different automata frameworks can be compared using functors.
- As [CP'20] do for automata, here the author does it for transducers

- This work uncovers categorical structure behind transducers.
- The work on Bojańczyk on functions on strigs uses a type of lists. Here he
  works with Church encodings without a need of a special type.

The general theme is "implicit automata via proofs-as-programs". 

Polyregular functions [Boj18] have several characterizations among them as
mulit-head pebble transducers with stack discipline on pebbles. They can compare
positions of the pebbles. If this is not allowed one obtains comparison-free
class of the author.

## Results

- Characterizing classes of functions computed by transducers by typed \l-calculi.
- As [HK'96] theorem it uses also semantic evaluation to obtain the results, and
  it is not purely syntactic.
- It is possible that these equivalence results are indications of deeper
  structural connections between automata theory and lambada-calculus.



### Main resutls
Characterization of string-to-string functions in \lambda l\oplus\with calculus
(Dual Intuitinistic Linear Logic)
For simply tyed \l-calculus this is an open problem.

A new class of transductions. 
comparison-free polyregular functions are discovered by studing functions
definable in \lambda \ell^{\oplus\with}. 

#### Theorem 1.2.3**
Str -o Str regular string functions
Str -> Str comparison-free polyregular functions
Tree -o Tree regular tree functions

On a side result with a more syntactic approach:

Theorem 1.2.1 Characterization of star-free languages in terms of definability
by \l lP terms

Q: can we start with LTL syntax and avoid reference to Krohn-Rodes?

Q: expressiveness of afine calculi without additives? (aparently he has an
answer)? Is it true that presence of additive connectives makes a meaningful
reason in expressive power?

#### Categorical formalisation of transducers. 
He defines a notion of C-transducer then instantiates it in several ways:
SR: single state copyless streaming string transducers. Objects are finite sets
of registers and morphisms are copyless assignments. Then he can complete this
category with coproducts and products. This givees a symmetirc monoidal closed
category under some restrictions. So one can have a functor \Ell -> \Cc showing
that all functions defined by lmabda-terms are regular. 

Thm 1.2.4
SR_{\with\oplus} is a symmetric monoidal closed category
A result from category theory simingly unknown.

An interesting construction showing that under some assumptions
C_{\with\oplus}-transducers are equivalent to C_{\oplus} transducers. 
He also gives conditions on C guaranteeing that C-transducers are closed under
composition to the right with regular functions.
These allow to show give a different proof that copyless STT are closed under
composition [BC18]

#### Structural and separation results

Results on the number of pebles vs growth rate (pebble minimization result)
Characterisation as a composition of some basic functions
Some separation resutls: not all polyregular functions are comparison free, and
they are incomparable with HDT0L transductions.

Q: Layered streaming string transducers [DFG20] are between copyless and general
STT. How far form copyless they are? Can we get a characterisation for them?

#### Related work

There is a work of Selier characterizing k-head two-way non-det automata by
some semantic object inspired by linear logic [Sei18]. It is not obvious what
the syntax would be for this thing. The encoding of strings is a semantic
version of this in the thesis

Q: Where the idea of the encoding of strings comes from? This is very useful.

Q: Salvati's definition of recognizability. Relation with his definition for
strings that can be then lifted to a definition for \l-terms. Is it the case
that in type \string[\t] we recognize sets of terms that are exactly regular
languages when using Salvati's definition? (page 37)

Q: Claim 1.4.2 Class \E is the same as functions definable by safe \lambda-terms
in Tree_\G[\tau]->\Tree_\S. What is the status of this claim?
He wants also to find a transducer counterpart of collapsible pushdown automata
(stack is initialized with the input tree?) that compute exactly the simply
typed \l-terms of type Tree_\G[\tau]->Tree_\S

Claim 1.4.6 He gets the same results as in the thesis when he removes additive
connectives but adds afifineness.

Claim 14.



   

## Comments
- These est remaquablement riche. Elle est exceptionalement riche. 
- This thesis certainly pushed me outside of my confort zone.
- It is possible that the results of this thesis indicate deeper connections:
  chercher des raisons profondes et structureles entre automata theory and lambda-calculus.
- Some highlights:
  - very elegant definition of comparison-free polyregular function: relation to
    pebble transducers, hierarchy of growth speed characterized by the number of
    compositions.
  - Categorical generalization of transducers: does it come from understanding
    that \Ell-setting computes exactly functions definable in the
    lambda-calculus? Categorical monoidal-closed.
  - The role of different function spaces used to represent the type of
    functions on strings: fleche lineaire -o gives regular functions, and fleche
    classique -> gives  comparison-free polyregular.
  

# Questions
0. What is the intuition behind composition-by-subtitution operation? Did you
   have it by looking like terms work? For example reverse is programmed by
   changing each letter to a piece of code.
1. Does \Ell-setting  come from understanding  that \Ell-setting computes
   exactly functions definable in the  lambda-calculus? \Ell is initial among
   all reasonable streaming settings.
2. You mention several times that instead of addtive connective one could try to
   work with afine types. Claim 1.4.6 says that one would get similar resluts.
   Have you advanced on this? What about the whole class of polyregular
   functions? Is there a chance to capture it with some \lambda
4. Characterization of polyregular by Bojanczyk with build list type is
   of different than his. How you can compare two styles of characterizations.
3. Theorem 1.2.1 about star-free languages goes through Kroh-Rodes because it
   uses decomposition. Could it be possible to start direclty from LTL?
4. Salvati's definition of recognizability. Relation with his definition for
strings that can be then lifted to a definition for \l-terms. Is it the case
that in type \string[\t] we recognize sets of terms that are exactly regular
languages when using Salvati's definition? (page 37)
6. Class of high iterated pushdown tree transducers (Engelfiet & Vogel). Closure
   of macro tree transducers under composition.
   The question of what can compute all and safe \lambda-terms in Tree types. 
   Claim 1.4.2 Class \E is the same as functions definable by safe \lambda-terms
in Tree_\G[\tau]->\Tree_\S. What is the status of this claim?
He wants also to find a transducer counterpart of collapsible pushdown automata
(stack is initialized with the input tree?) that compute exactly the simply
   typed \l-terms of type Tree_\G[\tau]->Tree_\S. This is related to Conjecture
   1.4.3 of characterizing a transducer counterpart of higher-order collapsible
   pushdown automata. 
7. He says that finite automata are "arguably not very well-behaved as a complexity
   class". Why? Ensebles rationels et recursifs.


