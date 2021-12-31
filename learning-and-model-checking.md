# learning and model checking

[peled-adaptive-mc]
[Peled, D., Vardi, M.Y., Yannakakis, M.: Black Box Checking. In: Wu, J.,
Chanson, S.T., Gao, Q. (eds.) Proc. FORTE ’99. pp. 225–240. Kluwer Academic
(1999)]

A paper on using learning to do parametric verification
[learning-parametric-verification.pdf]
"Learning to Prove Safety over Parameterised Concurrent Systems", Anthony W. Lin
It has a list with references to many examles. 


[Chow-TSE87]

To see how learning is used in MC I have looked at "Adaptive Model Checking "
  * It may be interesting to rework Anguin's algorithm for negotiations. The
    algorithm uses Vasilevskii and Chow black-box test algorithm that is
    interesting to implement for negotiations too. 
	*	This business of MC with learning is a bit strange since essentially we need to learn the whole model. Maybe the gain is that we do not know what is the size of the system so we learn a model assuming size n. If it model-checks and it is conform according to VC-test wrt to size n then we just stop (why this is sound). Otherwise we have either a counterexample from MC or a counterexample from VC, and we continue learning. (why this is sound).
	*	For VC procedure the parameter is the number of states. We may think the same for negotiations assuming that we know distribution of actions over processes. 
	* The idea of VC is quite simple. We use a spanning tree T of a model M to have access paths to every state of M. From there we play a sequence of length n-m so that we are sure to access every state of B (it looks that T gives also a spanning tree of B). Then we verify that every state of B has the same signature as a state of M, and that after one step the results also have the same signatures. 

#learning