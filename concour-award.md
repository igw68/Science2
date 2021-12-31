CONCOUR'21 award 

Luca: You receive the CONCUR ToT Award 2021 for your paper On the Expressive Completeness of the Propositional mu-Calculus with respect to Monadic Second Order Logic, which appeared at CONCUR 1996. In that article, you showed what I consider to be a fundamental result, namely the mu-calculus and the bisimulation-invariant fragment of MSOL have the same expressiveness over transition systems. Could you tell us how you came to study that question and why do you think that such a natural problem hadn't been answered before your paper?

David and Igor:
At that time we were interested in automata characterizations of the
expressive power of MSOL (monadic second-order logic) and the mu-calculus. In
1988 Damian Niwinski has shown that over binary trees the mu-calculus and MSOL
are expressively equivalent. When it appeared, the result was quite surprising,
even unexpected.  The two logics are not equivalent on unranked trees where the
number of children of a node is not  fixed. In consequence, the logics are not
equivalent over the class of all transition systems.

In 1983 van Benthem showed that modal logic is equivalent to the bisimulation
invariant fragment first-order logic. When we have learned about this result we
have realized that our automata models can be used to prove a similar statement
for the mu-calculus. 

The method of van Benthem could not be applied to MSOL, the automata based
method looks like the only way to prove the result. 

Luca: I am interested in how research collaborations start, as I like to tell "research-life stories" to PhD students and young researchers. Could you tell us how you started your collaboration?

David: I came to meet Igor when he was visiting Bordeaux in fall 93, presenting his first completeness result on a proof system for the mu-calculus (LICS 93). I was myself starting a PhD considering modal logic for specifying (various form of) non determinisms in link with (power) domain theory (FST&TCS 93).

We eventually met again in Auvergnes (center of France) for the Logic Colloquium in summer 94. There, spending time in the parc nearby the conference venue or walking around the volcanoes, we elaborate a notion of non deterministic automata for the modal mu-calculus. This result can be seen as extending the notion of « disjunctive » normal form from propositional logic to the modal mu-calculus. I remember that Igor later used this result for his second completeness result with Kozen’s proof system proposal for the mu-calculus (LICS 95). Thanks to Igor, this was for me the occasion to learn in the depth the link between mu-calculus and tree automata.

Incidentally, Johan Van Benthem was also attending this Logic Colloquium and we both attend his lecture about the bisimulation invariant fragment of FO. Although we did not yet realize we could generalize his result to MSO, this surely increases our own understanding of logic.

Our first result (Automata for the mu-calculus) was presented at MFCS in 95 in Pragues where Igor and I met again. It could have been there, or a little later that we eventually postulate our bisimulation invariance result. However, proof arguments were only found later exchanging emails. It was a bit amazing for me that we could discuss that way across Europe: email started to be heavily used only in the late 80's. In my head, Poland was far far away from France.

Yet our collaboration was eventually in the line of an  ongoing collaboration
between Warsaw and Bordeaux, involving researcher like Arnold (my supervisor)
and Niwinski (Igor's mentor), both major specialists in the area of automata and
logics. Somehow as a followup, together with Aachen (Graedel and Thomas) and
many other sites, the GAMES European network was later created, and, almost at
the same time, Igor came to Bordeaux as a CNRS researcher.

Luca: As far as I know, van Bentham has shown (https://pure.uva.nl/ws/files/3800551/1170_12194y.pdf) that modal logic has the same expressive power as the bisimulation-invariant fragment of first-order logic. In some sense, one may consider your main result as the extension of van Bentham's theorem to a setting with fixed-points. Could you briefly describe at a high level the challenges that fixed-points created in your work? To your mind, what was the main technical achievement or technique in your paper?

David and Igor: Sure our result is similar by van Benthem's, and, as mentioned
above, his own presentation in 93 was very inspiring. However, his proof relies
on compactness of first-order logic and cannot be adapted to monadic
second-order logic. We have used automata techniques. 

In our previous works we have developed automata models for MSOL and the
mu-calculus on unranked trees. Every transition system is bismulation invariant
to a tree obtained by the unfolding of the transition system. Crucially for our
result, it is also equivalent to a tree where every subtree is duplicated
infinitely many times. A short pumping argument shows that on such trees the two
automata models are equivalent. 

Luca: Did any of your subsequent research build explicitly on the results and the techniques you developed in your award-winning paper? Is there any result obtained by other researchers that builds on your work and that you like in particular?

David and Igor: Around that time Marco Hollenberg and Giovana D'Agostino have
used our automata method to show the uniform interpolation property for the
mu-calculus. 

In collaboration with Giacomo Lenzi (postdoc in Bordeaux from Pisa), David
considered the bisimulation invariant fragment of various levels of the monadic
quantifier alternation hierarchy. It turns out that monadic Sigma_1
corresponds to reachability properties and monadic Sigma_2 corresponds to Buchi
properties, respectively first and second level of the mu-calculus hierarchy. 

It could be the case that the all mu-calculus can be translated into monadic
Sigma_3 formulas -- this is true when restricting to deterministic transition
systems. However, with non determinism, such a result seems difficult to
achieve. 

Incidentally, Giacomo and David also proved that adding limited counting capacity
to modalities yields a fixpoint calculus equivalent to the unraveling invariant
fragment of MSO (LICS 2001).  

In 1999 collaboration with Erich Graedel, Igor has used similar techniques to define
and study guarded fixpoint logic. Subsequently, several other fixpoint logics of
this kind were proposed with the most expressive one probably being guarded
negation logic with fixpoints of Bárány, ten Cate, and Segoufin from 2015. 
These works all use automata theoretic method to some extent. 

Luca: Your paper was written while Igor was at BRICS at the University of
Aarhus. Igor, what was it like to be at BRICS@Aarhus at that time? What role do
you think centers like BRICS played and can play in the development of
theoretical computer science? Do you think that your stay at BRICS had a
positive impact on your future career?

Igor: My stay at BRICS had definitively a beneficial impact on me. At that
time BRICS was one of the most active centers world wide in theoretical computer
science. Being able to see and talk to so many different people, being exposed
to so many different ideas, was very enriching. BRICS was a meeting place 
allowing scientists to have a better and larger vision of our field.
BRICS contributed to the development of many people involved, as well
as to the excellence of Aarhus, and even Denmark as a whole, in our field.

Luca: I have been brought up in the concurrency-theory tradition and I feel that bisimulation-invariant properties are the interesting ones over transition systems. Do you think that we actually "need" logics that allow one to specify properties of transition systems that are not bisimulation invariant?

David: That was the idea indeed and the mu-calculus is the good logic
for that. From a mathematical perspective, bisimulation is a fairly natural
definition. In some sense, bisimulation equivalence is a greatest co-congruence.

However, I always suspected that bisimulation is too much a fine grained equivalence for concurrency. When modeling realistic system, non determinism arises either as controllable (angelic) or uncontrollable (demonic) choice. In this case, the right equivalence to be considered is double simulation.

The funny thing is that David Park, who "invented" bisimulation, was actually studying equivalence of J.R. Buchi deterministic string automata where, because of determinism, bisimulation turns out to be equivalent to double simulation. It is only after Matthew Hennessy and Robin Milner work in concurrency that bisimulation was applied to non deterministic behaviors.

Igor: In the context XML and semistructured data, bisimulation is not relevant. One
of the prominent queries in XPATH is whether a value appears twice -- that is clearly
not a bisimulation invariant property. So while XPATH looks very close to PDL or
the mu-calculus, many techniques and questions are very different. The other
context that comes to mind is controller synthesis, where we ask for a
transition system of a specific shape ex. with self-loops on certain actions.
Such self loops represents invisibility of the action to the controller. 


Luca: What are the research topics that you find most interesting right now? Is there any specific problem in your current field of interest that you'd like to see solved?

David: In Logic for Computer Science, there have always been two kind of approaches : model theory that eventually led to model checking and proof theory that eventually led to typed programing languages.

Twenty years later, aiming at designing and implementing real concurrent
systems, especially for interactive arts, I realized that the later approach was
(at least for me) a lot more effective. Building concurrent systems by
synchronizing arbitrary sub-systems sounded for me like unstructured
programming; it was essentially unmaintainable. Monads and linear types, among
many other approaches in typed functional programing, surely offered interesting
alternatives to process calculi approaches.

Igor: In the context of the paper we discuss here, I am surprised by
developments around the model-checking problem for the mu-calculus. After some
years of relative calm, Calude, Jain, Khoussainov, Li and Stephan have made an
important breakthrough in 2017. Yet, despite big activity after this result, the
research on the problem seems to hit one more barrier. 
Another old prominent problem is decidability of the alternation hierarchy for
the mu-calculus. The problem is: given a formula and a number of alternations
between the least and the greatest fixpoints, decide if there is an 
equivalent formula with this number of alternations. Even when the number of
alternations is fixed we do not know the answer. Among others, Thomas Colcombet
and Christof Loeding have done very interesting work on this subject.

Luca: What advice would you give to a young researcher who is keen to start working on topics related to automata theory and logic in computer science? 

David: From the distance, our result sounds to me as a combination of both technique and imagination. Technique for mastering known results and imagination for finding original open problems, especially between research fields that are not (yet) known to be deeply related. As a matter of fact, I felt lucky finding such a fresh open problem that was (probably) a lot easier to solve than many other well-known hard problems.

Technique comes from hard work. It is obviously essential but somehow easy to teach and evaluate in academia. Imagination come from curiosity. It is still essential but a lot more difficult to teach. So young researchers must develop by themselves their own imagination and curiosity.

In the automata theory branch of logic in computer science, the remaining open
problems seem fairly hard, so I believe that it is young researcher imagination
that will make the difference for setting up new interesting direction of
research, especially those who are ready to look aside, towards other areas of
logic in computer science and, because it can be a considerable source of
motivation, funny applications.

Igor: 
Naturally, the field is much broader these days than it was 25 years ago. It is
crucial to master some techniques. For this, working on variations of already
solved problems is a good method. Yet, I think it is important to escape
the cycle of constant modifications of existing problems and their solutions. 
I would suggest that at some moment one should find an important open
problem that one is passionate about and should spent a considerable effort on
it. I admit that this is a meter of a taste, personality, and having a sufficiently
comfortable situation to afford such a risk. Another good option is to
look at frontiers with other areas: distributed computing, semantics,
control theory, security. 



