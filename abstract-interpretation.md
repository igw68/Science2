# Abstract interpretation

jones-nielson-static-analysis.pdf

The goal of abstract interpretation is to obtain as much information as possible
about a program's possible run time behavior without actually having to run it
on all input data; and to do it automatically.

There are many possible analyses: [[examples-of-program-analyses]]

## May influence: 
compute the set of variables on which the value of $f(x_1,\dotts,x_n)$ depends
in *at least one computation*. This is useful at partial-evaluation, to mark
which expressions  are unknown.

## Must influence:
compute the set of variables on which the value of $f(x_1,\dotts,x_n)$ depends
in *every computation*. This is used in lazy evaluation to say detect that some
arguments may be immediately computed

# Q: 
What about a more general schema: some trace of a program is in the language of
a deterministic automaton $\Aa$; or every trace. Here the questions look like
the same since we can complement $\Aa$. If $\Aa$ is nondeterministic then they
are not the same. 

[[abstract-interpretation-cannot-be-homomorphic]] So we usually have an order on
the abstract domain corresponding to the level of knowledge.

# Q: What is a difference between abstract interpretation and verification?
Looks like methods are different, but the goal is the same. 

[//begin]: # "Autogenerated link references for markdown compatibility"
[abstract-interpretation-cannot-be-homomorphic]: abstract-interpretation-cannot-be-homomorphic "Abstract interpretation cannot be homomorphic"
[//end]: # "Autogenerated link references"