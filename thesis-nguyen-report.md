
This a remarkable thesis establishing equivalences between definability of
string-to-string functions in certain lambda-calculi and transducers.
The thesis presents also interesting equivalences for counter-free automata and tree-to-tree
transducers.  
To simplify the report I will only discuss them only at the very end. 
Even when restricted to results on string-to-string functions the thesis
contains an impressive volume of new concepts and results. 

The main results of the thesis are characterizations of string-to-string
functions definable in linear $\l$-calculus. 
If definable is understood as a linear function space then the corresponding
class is the standard class of regular string transductions.
If classical (non-linear) function space is used then the corresponding class is
that of comparison-free polyregular functions. 
This is a new class that lies strictly between regular and polyregular
functions.
Apart this characterization result, the thesis gives a number of results on the
new class of transducers: (i) several different characterizations of the class
including a pebble machine model, and (ii) a pebble minimization result.
This gives a convincing set of arguments for making the newly introduced class
interesting. 

The thesis starts with a long introduction giving an unusually large context
of the work presented in the thesis.
It gives an opportunity to appreciate the width of interests of the author, very
good knowledge of the literature, and his ability to make connections between
different branches of theoretical computer science. 
Actually, the whole thesis is a proof of this very precious capability. 
In my opinion the starting point of the thesis is a remarkable, and not
well-know, theorem of Hillebrand and Kanellakis from 1996: a language is regular,
if and only if, it can be defined by a simply typed $\l$-term using Church encoded strings. 
The thesis provides results of a similar kind but for transducers instead of
finite automata and a variant of linear $\l$-calculus. 

Since the thesis extends the approach of Hillebrand and Kanellakis, it is
important to go bit deeper in the formulation of their theorem. 
This will also help to understand the contributions of the thesis.

It is well known that strings can be encoded as $\l$-terms of type $o->o$. 
For example $abc$ is encoded as $\l x.a(b c(x)): o->o$. 
So a term of type $(o->o)->Bool$ determines a set of words, a language in terms of
language theory.
It is then natural to ask what kinds of languages are definable by terms.
It is known that for the above encoding not all regular languages can be
defined by simply-typed $\l$-terms.
To capture regular languages, it is necessary to go to more complicated types. 
If we denote type $o->o$ as $String[o]$ then we can also consider $String[\tau]$ for
arbitrary simple type $\tau$. 
The theorem says that every regular language can be defined by a term of type
$String[\tau]-> \Bool$, for some $\tau$ depending on the language. 
The theorem also says the converse, which is more difficult as it is not easy to
understand the structure of terms in $String[\tau]-> \Bool$.
The proof avoids this problem by using a very elegant
semantic argument. 
In Church encoding string concatenation corresponds to a
composition of terms. 
Hence in a finitary model of a simply typed $\l$-calculus type $String[\tau]$ is
a finite monoid wrt.\  concatenation. 
This monoid can be used to recognize the language defined by a term of type
$String[\tau]-> Bool$.
To summarize, the main idea behind Hillebrand and Kanellakis argument is to consider types
$String[\tau]$ and use monoid structure in a model to prove the difficult direction
of the theorem. 

The thesis builds on this idea to understand not automata, that are string
acceptors, but transducers, that transform strings to srtings. 
This demands several conceptual advances.
First is to find a fragment of the lambda-calculus that is expressive enough and
yet manageable enough for some syntactic arguments. 
Here linear lambda calculus is chosen.
At least as important is to find a semantic framework for representing
transducers. 
The proposed notion of streaming tree transducers indexed by a category is very
elegant, and is a workhorse behind many results of the thesis.
Finally, there is a new notion of comparison-free polyregular functions and
transducers that is exactly right to make the correspondence go through. 

This maybe a good place to make a summary of the content of the thesis. 

Section 2 defines different types of transducers and summarizes relations
between them. The section has a lot of content. 
The author makes a very good job of presenting in a compact way many approaches of
defining string-to-string functions and the relations between these approaches. 
A class of regular functions is defined as those realizable by copyless
streaming string transducers [Alur & Cerny'10]. 
The bigger class of polyregular functions [Bojanczyk'18] serves as a starting
point of the main object of the thesis that is comparison free polyregular functions. 
Recent results on layered SST and their relation to copyless/copyfull SST, as
well as to HDT0L are also presented.  

Section 3 introduces the class of comparison free polyregular functions
(cfp-functions). 
These is the smallest class containing regular string functions and closed on
composition by substitution. 
The author also gives a machine characterization: machines with stack like
pebble management. Once again it almost the same model as for polyregular
functions but comparisons between pebbles are disallowed. 
This is maybe the best motivation for the name "comparison-free" although these
machines play very little role in the thesis. 
Yet, there are very interesting results about these machines showing exact
correspondence between growth rate of the output and to the minimal number
pebbles needed to realize a given function. 
Other important results of this section are separation results showing that
cfp-functions lie strictly between regular and polyregular functions, and are
incoparable with HDT0L transductions. 
On the way a very elegant characterization of cfp-functions over one letter
output alphabet  is given.
The most important result of this section is the closure of cfp-class by
standard composition. 
As a side result the author obtains another two characterizations of cfp-class.
Polyregular funcitons of Bojańczyk are compositions of  regular functions and
squaring with underlining.
Comparison-free variant uses a weaker version of this squaring operation with
"very weak form of underlining". 
Every cfp-function can be also presented as a composition of a regular function
and iterated weak squaring function. 


Section 4 introduces a categorical formulation of streaming string transducers
(STT). 
The main idea is to take objects in a category instead of registers and
morphisms between objects instead of operations on registers. 
This is called streaming setting.
This is very elegant approach related to recently introduced categorical
automata of Colcombet and Petri\,san.
The power of this abstraction can be seen in first, very simple, result: if
there is a functor a streaming setting over a category C to a streaming setting
over category D then D-SST are at least as expressive as C-SST.
This allows for example to formalize a state elimination result in a more
general setting: every C-SST is equivalent to one state C'-SST for suitable C'. 
While such a construction was known for particular SST's, an abstract version is
very handy in the later developments.
Naturally copyless SST can be presented in this framework. 
More interestingly, the generalization leads to a natural generalization of
copyless SST where intuitively "the set of registers depends on the current
state". 
This version is shown equivalent to SST with one state thanks to general
arguments on level of categories.
The generalization is very useful in later constructions. 
The most important advantage of streaming settings is that they allow to study
abstract notions of co-product and product completions that turn out to be
related to adding states and nondeterminism respectively. 
The end result is that when we start with a basic category for copyless SST and
add products and coproducts in a free way, we obtain the setting that is still
equivalent to copyless SST.

Section 5 presents the main results of the thesis that are equivalences between
versions of definability in $\lwith$-calculus and versions of SST transducers.
The calculus in question is based on propositional linear logic with
multiplicative and additive connectives. The linear variables must be used
precisely once, unlike in affine setting where they can be used at most once.
Linear arrow allows for a more precise Church encodings of strings. 
The fundamental property of these encodings is that there is a bijection between
strings and normal forms of terms in the type of strings. 
This is a difficult result on normalization in $\lwith$-calculus that takes a
good number of pages to prove. 
Once encodings are decided, the second choice is how functions from strings are
represented.
They can be either terms of type String[\tau]-o String[\tau] or of type
String[\tau]-> String[\tau].
The main result of the thesis is that the first choice corresponds to regular
functions, and the second to cfp functions. 
The proof for regular functions is very interesting, essentially using the
categorical development from Section 4.
First a streaming setting from $\lwidth$ is defined. 
Then it is shown that  single state $\Ell-SST$ computable functions are exactly $\lwidth$
definable (with linear function space).
The right-to-left inclusion is based on the understanding on the shape of the
normal forms in $String[\tau]-o String[\tau]$.
The last important step is to show that every  $\Ell-SST$ function is regular. 
This is by showing that $\Ell$ setting is in some sense initial among all
settings with certain properties. 
Since $GR$-setting corresponding to regular functions satisfies this properties,
one gets a morphism from $\Ell$-setting to $GR$-setting, and the general result
about expressibility allows to conclude.

The main result on comparison-free polyregular functions builds on the previous
one. 
Recall that cfp-functions are obtained from regular functions by composition by
substitution. 
By the result described in the previous paragraph, regular functions are
definable in $\lwidth$. 
So it is enough to show that composition by substitution is expressible in
$\lwidth$-calulus. This is a realtively simple.
The other direction is much more difficult. 
It relies on understanding what are shapes of terms in type String[\tau]\to
String[\s]. 
This is more difficult than in the previous case as here we have a non-linear
function space.


