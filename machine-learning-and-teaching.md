# Machine learning and teaching
Jerry Zhu
[https://simons.berkeley.edu/talks/tbd-288]

# Passive learning
* X : input space (Nat or \Rr^d)
* Y: output space eg {0,1}
* h: X-> Y a hypothesis. Eg function h_i(x)=1 if x>=1
* H is a subset of X-> Y the hypothesis space
  * Say H={h_i : i\in \Nat}
* Target h*: X->Y
  * h* can be *realizable* when it is in H, but it may also be *agnostic*.
  
## Passive learning protocol
* Environment has $P(x,y)$ 
  * P(y|x)=1[y=h*(x)] this is distribution on x that put all weight on h*(x)
* Environment draws a training set S={(x_1,y_1),\dots,(x_n,y_n)}
  * S\sim P(x,y), S approximates P(x,y)
* Learner receives S and selects \hat h\in H. We just choose one function that is
  compatible with S.
  * this is OK because machine learning cares only about **small risk**
* Loss l(y,y')>-0. Ex l(y,y')=1 iff y-y'
* True risk R(h)=E_p(l(h(x),y))
  * Learners goal is to get small R(h) not h=h^*.
  * Empirical error on S: \hat R(h)=1/n\Sum^n_(1,n)l(h(x_i),y_i)
* Empirical risk minimization
  * ERM: find \hat h minimizing empirical risk. There may be many \hath giving
    the minimum. 
	* the problem can come from overfitting
  	* R(h) >> \hR(\hath)
  	* R(\hh) >> R(h*)
  	* no good function \hh in H
* Risk decomposition
  * Bayes error R(h*) this is the fault of distribution P
    * This is unavoidable, linked to P
  * Approximation error, what is the best h' I can get to approximate h*
    * This is problem of H. Considered as modelisation problem.
  * Estimation error: how far \hh from the best h'
    * All machine learning concerns with this error
* Probably-Approximately-Correct Guarantee (PAC)
  * Theorem: Probability of quite good S is large. If S has size n then the
    estimation of error is 1/\sqrt(n).  The bound uses the size of H, so we can
    tolerate exponential size of H, but not an infinite one.

##  Vapnik-Chervonenkis dimension
* VC(H) allows to use infinite H spaces
* VC(H) the larges t such that there are {x_1,..x_t} such that members of H can
  assign every possible 2^t result vector to these values.
* Example: VC(H) for the set from the example above is just 1.
* Now new version of PAC theorem gives dependency of error on VC(H) and not the
  size of H.

## Summary
This is passive learning because we just get S from somewhere, and we need to do
something with it. 
VC(H) allows to work with infinite spaces H.

# Active learning



  