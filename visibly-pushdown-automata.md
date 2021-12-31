# Visibly pushdown automata

## On trees
- Alur Madhu paper [alur-visibly-pushdown-tree.pdf]
- Bozzeli paper [bozzeli-alternating-visibly-pushdown.pdf]

Alternating pushdown visibly-automata are decidable on words
Thm [Bozzeli]: Emptiness of alternating VPA on words is 2-EXPTIME complete. 

For alternating VPA on trees the emptiness problem is undecidable
[alur-visibly-pushdown-tree.pdf].
The reduction is to PCP in the same style as Joly's reduction. 
We have a word with dangling branches that indicate how many pop's to do to
recover the link.
One maybe can get a nicer one if one considers encoding of a queue machine. 

