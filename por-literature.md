# POR literature

date: [[2021-06-09]]


## Most relevant papers
* Parosh Abdulla, Stavros Aronis, Bengt Jonsson, and Konstantinos Sagonas. 2014.
  Optimal dynamic partial order reduction. In POPL 2014. ACM, New York, NY, USA,
  373ś384. https://doi.org/10.1145/2535838. 2535845, And the JACM final version

* Vafeiadis, POPL'2022 TRust [vafeiadis-popl22.pdf]

* Kokologiannakis, M., Raad, A., Vafeiadis, V.: Effective lock handling in
  stateless model checking. Proc. ACM Program. Lang. 3(OOPSLA) (2019) doi:
  10.1145/ 3360599 
	Probably describes another approach to DPOR than Parosh
	[vefeiadis-effective-oopsla19.pdf]
  [[por-locks]]

* Kokologiannakis, M., Raad, A., Vafeiadis, V.: Model checking for weakly
  consistent libraries. In: PLDI 2019, ACM, New York, NY, USA (2019). doi:
  10.1145/ 3314221.3314609 
	[libraries-vafeiadis-pldi19.pdf]
  [libraries-vafeiadis-pldi19-full.pdf]
	Apparently there is a review of other DPOR methods in this paper.
  

* BAM: Effcient Model Checking for Barriers, Vafeiadis, V, NETSYS'21
  [[por-and-barriers]]
  [vefaiadis-netys2021-barriers.pdf]

* Bounded Partial-Order Reduction, Coons, Musuvathi, McKinley, OOPSLA’13,
  [[bouded-dynamic-por]]
  [bpor-oopsla-2013]
  Interesting combination of Dynamic POR and bounded number of preemptions. 

* Monotone partial-order reduction [kaholn-cav09.pdf]
  Defines normal forms for traces and explores only normal forms.
  
## POR and symmetry reduciton
- Emerson, Jha, Peled, 1997 Combining Partial Order and Symmetry Reductions, 
  [emerson1997_Chapter_CombiningPartialOrderAndSymmet.pdf]

## Stubborn sets
- Stubborn Set Intuition Explained, [valmari-stubborn-intuition.pdf]
  A nice paper giving all basic definitions and comparing to persistent sets.
  [[stubborn-sets]]

- Stop It, and Be Stubborn! [valamri-stubborn.pdf]
  Interesting restriction to may-terminating systems that simplifies POR method. 

## Bounded partial-order
[bpor-oopsla-2013.pdf]
[Bounded Partial-Order Reduction, Coons, Musuvathi,  McKinley, oopsla'13]
Preemption bound: a preemption is switching a process even if it has some
enabled action. 
They want to explore runs with a fixed number of preemptions.
They show how to do it while using POR at the same time. 
This is not obvious as stopping because of preemption can make POR not sound. 
I do not really understand what they are doing.

## Others
* David Baelde, Stéphanie Delaune, and Lucca Hirschi. POR for security protocol equivalences – beyond action-determinism.
  Looks like a different application area. 
	[delaune-por.pdf]
	[[por-for-security]]

* Marek Chalupa, Krishnendu Chatterjee, Andreas Pavlogiannis, Nishant Sinha, and
  Kapil Vaidya. 2017. Data-centric Dynamic Partial Order Reduction. Proc. ACM
  Program. Lang. 2, POPL, Article 31 (Dec. 2017), 30 pages.
  https://doi.org/10.1145/3158119 
* Jeff Huang. 2015. Stateless model checking concurrent programs with maximal
  causality reduction. In PLDI 2015. ACM, New York, NY, USA, 165ś174.
  https://doi.org/10.1145/2737924.2737975 
* Naling Zhang, Markus Kusano, and Chao Wang. 2015. Dynamic partial order
  reduction for relaxed memory models. In PLDI 2015. ACM, New York, NY, USA,
  250ś259. https://doi.org/10.1145/2737924.2737956 	
* Parosh Aziz Abdulla, Mohamed Faouzi Atig, Bengt Jonsson, and Tuan Phong Ngo.
  1.    Optimal Stateless Model Checking Under the Release-acquire Semantics.
  Proc. ACM Program. Lang. 2, OOPSLA, Article 135 (Oct. 2018), 29 pages.
  https://doi.org/10.1145/3276505 
* Michalis Kokologiannakis and Konstantinos Sagonas. 2017. Stateless Model
  Checking of the Linux Kernel’s Hierarchical Read-copy-update (Tree RCU). In
  SPIN 2017. ACM, New York, NY, USA, 172ś181. https:
  //doi.org/10.1145/3092282.3092287 
* Stateless Model Checking under a Reads-Value-From Equivalence, Pratyush
  Agarwal, Krishnendu Chatterjee, Shreya Pathak, Andreas Pavlogiannis, Viktor
  Toman,  CAV 21


## Coarser paritionning
* Albert, E., G´omez-Zamalloa, M., Isabel, M., Rubio, A.: Constrained dynamic
  partial order reduction. In: Chockler, H., Weissenbacher, G. (eds.) CAV 2018,
  pp. 392–410. Springer International Publishing, Cham (2018). doi:
  10.1007/9783-319-96142-2 24 
* Aronis, S., Jonsson, B., L˚ang, M., Sagonas, K.: Optimal dynamic partial order
  reduction with observers. In: TACAS 2018, LNCS, vol. 10806, pp. 229–248.
  Springer, Heidelberg (2018). doi: 10.1007/978-3-319-89963-3 \ 14 


## General parallel programming

The Art of Multiprocessor Programming, Maurice Herlihy, and Nir Shavit, Book
[multiprocessor-programming.pdf]

Java concurrency in Practice, Book, Many authors
[]
	#distributed
#partial-order

