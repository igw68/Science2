# Semantic optimization of querries

Diego Figuera
Rewrite a query to an equivalent one in a tractable class
Here translating conjunctive queries into conjunctive queries of small
tree-width

- CQ evaluation is |D|^|q| it is W[1]-hard in parametrized complexity
- For tree-width k it is tractable in |D|^k|q|
  
- Problem: Given q\in CQ is there q''in TW_k st q\equiv q'

- Thm The semantic width-k problem is NP-complete [Dalmau,Kolaitis, VArdi'02]
  - compute core(q) and this gives the minimal tree-width
  - Problem: computing core(q) is a NP-comlete

- If we know that a query is equivalent to TWk then we can evaluate it fast. [Chen,Dalmau'05]

- Thm [Grohe'07]: A class of CQ has a tactable evaluation problem iff C has bounded
  tree width.

- Why bounded TW queries are easy:
  - existential EF game. Spoiler and dublicator play each on their own structure.
  - There are k mmoves, so this can be decided in PTIME.
  - Thm: duplicator has a winning strategy if q_1 q_2 map homomorphically to the same queries of
    TW_k

- What about the same thing with constraints?
  - A constraint is a DB property
  - Here we do the same but inside databases satisfying the constraint.
- Types of constraints
  - tuple-generating dependencies (existential datalog rules)
    - \forall x\forall y q(x,y)-> \exists z p(x,z)
  - equality generating dependencies:
    - \forall q(x) -> y=z for some vars y,z in x
  
	-Thm The semantic tree width-1 problem is undecidable [Figuera et al 20]

- For every \gamma\in TGD querry which is tw-preserving and query. If q has TW_k
  tne you can find a small equivalent TWk query. This gives dedcidability






#RATIO
#seminar 2021-05-10