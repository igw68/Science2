# Well-quasi-orderings

WQO are used for checking reachability properties of transition systems.

[kruskal-wqo.pdf] Kruskal WQO: a frequently rediscovered concept.
An overview paper [abdulla-wqo.pdf] discusses WQO-transition systems.


## Definitions
- reflexive and transitive relation such that 
  - for every infinite sequence there are $i<j$ with $s_i< s_j$.
- 
## Constructing WQO
- Base WQO's are $(A,=)$ or $(\Nat,\leq)$.
- Below we assume that $(A,\leq)$ is a WQO
  - [Highma's Lemma] $(A^*,\leq^*)$ is a WQO; where $\leq^*$ is embedding relation on sequences.
  - [Finite powersets] $(P_{fin}(A),\leq_P)$ is WQO; $\leq_P$ is covering order
    (for every element there is a bigger element).
  - [Finite Multisets] S\leq S' if there is an injection f from S to S' with a\leq
    f(a). This is a special case of Highman's Lemma
  - [Vectors of size k] with coordinatewise ordering. Once gain Highman's lemma
    where words are of identical length.



#Andrzej