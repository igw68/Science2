# Subject PhD: distributed



Synthesis for distributed systems: monitoring, control, and learning


Advisors: Anca Muscholl, Igor Walukiewicz (LaBRI)


Distributed systems are challenging because of non-determinism: even if every
process is deterministic, their parallel composition may have many executions,
 often exponentially many in the number of processes. For this reason the analysis of
 distributed systems is computationally difficult, and the reduction to an equivalent
 sequential system often unfeasible. But this "state explosion problem" can be turned
 into advantage when looking at the synthesis problem.


Synthesis asks to construct a device having a required input/output
 behavior. In this context the state explosion problem can be interpreted
 positively: a distributed device may be much smaller than a sequential one.
 Similarly for monitoring or control: a distributed device may be much smaller, and
 may not hamper a distributed system in its monitoring/controlling tasks.


Finally, for learning, the complexity depends, in most cases, at least
 exponentially on the size of the system. 


The goal of the thesis is to find algorithms for synthesis, control, monitoring,
 and learning distributed systems. We adopt a language-theoretic approach taking
 Zielonka automata as the basic model of distributed systems. Such an automaton
 is a parallel composition of ﬁnite automata synchronizing on common actions.
 The model is very general and close to 1-safe Petri nets, but with more structure. 
 The theory of Zielonka automata is quite rich. The questions mentioned above
 have already been considered for this model, but their general decidability remains
 largely open [1,2]. Controller synthesis for Zielonka automata has been also shown
 to be equivalent to some Petri games [3]. 


As a first step, we would look at these questions for a special class of Zielonka
 automata called negotiations [4]. This class has been introduced relatively recently,
 and it turns out to have interesting theoretical properties [5] that allow to expect a
 progress on the above questions.


1. B. Genest, H. Gimbert, A. Muscholl, I. Walukiewicz:
 Asynchronous Games over Tree Architectures. ICALP 2013.


2. A. Muscholl, I. Walukiewicz:


Distributed Synthesis for Acyclic Architectures. FSTTCS 2014.


3. R. Beutner, B. Finkbeiner, J. Hecking-Harbusch.


Translating Asynchronous Games for Distributed Synthesis. CONCUR 2019.


4. J. Esparza, D. Kuperberg, A. Muscholl, I. Walukiewicz:
 Soundness in negotiations. Log. Methods Comput. Sci. 2018.


5. Javier Esparza, Anca Muscholl, Igor Walukiewicz:
 Static analysis of deterministic negotiations. LICS 2017


##  Candidates:

### Corto 
Automates logiques jeux. 
1. Stefan Kiefer: theorie des mots
2. Liverpool Zimmerman temporal logic (hyper LTL, team LTL)
3. Thomas Colcombet: Separate regular languages by star-free languages
4. Christel Bayer: between games and verification: find a part of a system that
   is responsible for a property to be satisfied.
	 

#distributed 