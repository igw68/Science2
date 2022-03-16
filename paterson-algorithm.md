# Paterson algorithm



![picture 6](images/dca8201f1d27bc24d9f6be71cab2d586194b0ec5ceb125265e3a1e38221b19e1.png)  

The idea is that there is a wave of processes stopping at different gates Q.

This algorithm can be interesting for WW reduction. 
In the first wave all processes do $Q[i]=1$ and $T[1]=i$ 
These commute, but for the last write when using WW reduction. 
Unfortunately, there will be a lot of interleaving still because of $Q[k]<j$
test that will interleave with $Q:=j$ assignments.

The example comes from [valamri-stubborn.pdf]. 
Valmari can reduce the state space 3-fold. He says that the example is not
treatable with the standard symmetry reduction technique (because of the test in
await that is implemented as a for loop.)

#partial-order