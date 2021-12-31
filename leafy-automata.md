# Leafy automata


[[2021-07-12]] Dyskusja z Andrzejem
* Lepsze automaty
Nastepny krok to zmodyfikowac definicje automatu w ten sposob aby saturacja byla
konsekwencja definicji. Dobrze by bylo jakby tez indempontence bylo konsekwencja
definicji. Wydaje sie ze nastepujaca zmiana by dzialala:
  * Rodzic ma osobny stan kontrolny dla kazdego dziecka.: tlumaczenie linowe z i do algola
* Po tej definicji bedzie nas interesowala zlozonosc i rownowaznosc
* Zdefiniowac inaczej nawiasowanie w data-trees aby miec odpowiedniosc z game semantics
  * Dobrym przykladem jest fx. Jak my to robimy, to x jest pod f. W game
    semantics f i x sa obok siebie.
  * Aby to ominac mozna albo zdefniowac pseudo poziom dla wskaznikow
  * Albo wstawic x na tym samym poziomie co f jak sie tlumaczy fx
    Czyli sa dwa mozliwe kierunki: automaty prostrze albo trudniejsze, prostrze
    maja trudniejsza definicje rownowaznosci bo potrzebuja identyfikowac rozne wskazniki


[2021-07-12]] Automaty Stirlinga, i Higher-order matching
[[higher-order-matching]]
* Wydaje sie, ze automaty Stirlinga sa specjalna wersja class automata. Z drugiej
strony latwiej jest pracowac z register automata. Czy nie ma jakies translacji z
jedngo w drugie?
* Profile potrzebne do matching wydaja sie specjalne. 
  Ogolnie pustosc alternujacych automatow Stirlinga jest nierostrzygalna. To
  wynik z zakodowania Loadera. Wydaje sie jednak, ze do matching profile sa
  jakies specjalen
* Spojzec na dowod Loadera i starac sie zrozumiec roznice.
* (Z jakis powodow unarny PCF jest rozstrzygalny)
* Zobaczyc dowod Joly nierozstrzygalnosci, jest prostrzy niz Loader
  * [joly-loader-undecidability.pdf] w PDF Expert
* Barendregt ma przetrawione wyniki Loadera


Pierwszy krok to sprawdzic czy saturacja zachodzi
The CONCUR submission is [/Users/igw/Works/Andrzej/leafy_Concur.pdf]

The goal is to get some decidable fragments of 
**Finitary Idealized Concurrent Algol (FICA)**
[[finitary-idealized-concurrent-algol]]
We can hope to solve safety problem for some reduced cases but there is not much
hope for equivalence, as we cannot represent strategies uniquely.


**Concurrent Algol** has while, variables, and concurrency in a form of parallel
composition and semaphores. Moreover the subprocesses need to finish before the
process starting them can resume. 

[[game-semantics]] of FICA is captured by an **Leafy automaton**: automaton with
nested data in the form of a tree. 
This tree discipline takes care of most of
the dependencies between moves in game semantics.  
[[leafy-automata-reflections]]

Log:
* A resume of a situation at the CONCUR'20 submission [[leafy-automata-july-2020]].
* Some thoughts about improvements are [[leafy-automta-september-2020]]
* Meeting [[leafy-automata-5-oct-2020]]

Some things to improve after reports from FOSSACS:
* are leafy automata of some independent interest?
* It would be good to have a fragment with iteration.
* The correspondence with plays is not perfect because of saturation. 
* What is the complexity of the equivalence problem for LLA?
* Relation to truly concurrent games [Castellan, S, Clairambault, P.: Causality
  vs. interleavings in concurrent game semantics. In CONCUR 2016.]

#Andrzej

