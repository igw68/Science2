# Strategy improvement

## Nice idea of acceleration on progress measure. 
Antonio travail avec Pierre 

![picture 1](images/6365b0e49e317c1d8287a59405d225d3e8c866c3eb2ed00cd4b08f6a878f9de8.png)  

The idea is to accelerate when there is a hole in the tree. 
This prevents iterating in useless loops.
An example is 

![picture 2](images/c379131a03becbb5ae94a7ee9f386bdfef5a03f239f491ada4a96a8e299ba028.png)  

Here strategy improvement will iterate long time increasing signatures of 0 and
1, before going to 9. 
The algorithm has not choice because it want to get the smallest signature. 

Zielonka algorithm will be much faster here:
In the first decent it will mark 9 loosing, and detect 2 winning. 
Then it will convert 9 to winning and mark the rest as winning in two steps:
first 0 and then 1.

Q: How it translates in the context of fixpoint computation.

#Antonio