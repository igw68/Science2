# Simply typed lambda-calculus expressivity

# Simply typed lambda and regular languages
a language can be defined by a simply typed λ-term taking Church-encoded strings
as inputs if and only if it is regular [HK96, Theorem 3.4]. 
[Gerd G. Hillebrand, Paris C. Kanellakis, and Harry G. Mairson. “Database Query
Languages Embedded in the Typed Lambda Calculus.” In: Information and
Computation 127.2 (June 1996)]

There is a very simple proof of this result that is related to semantics
See [nguyen-thesis.pdf] page 18.

# Simply typed lambda-calculus captures elemetary functions.
Same [HK96]
simply typed λ-terms operating over certain data encodings and returning
booleans can compute all functions 28 in the complexity class ELEMENTARY (i.e.
those with a time complexity bounded by a tower of exponentials), and only
those. 

# Noramalization by  evaluation
Is this related to what we are doing?
Andreas Abel. “Normalization by Evaluation: Dependent Types and
Impredicativity.” Habilitationsschrift. Ludwig-Maximilians-University Munich,
May 2013. url: http: //www.cse.chalmers.se/~abela/habil.pdf 

#HOMC