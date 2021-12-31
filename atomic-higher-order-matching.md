# Atomic Higher-Order Matching
[padovani-models-decidable.pdf]
[clairablault-jeux.pdf]
This is a special case of HOM where the right hand-side is a constant of type 0.

* Outline: Celular terms. Every term is observationally equivalent to a celular term.

* Observational equivalence: 
  * for terms of type o when they are $\b$-equivalent
  * for other terms when for every argument they are equivent in o.

* Stretching lemma $\lambda \vec y. M[u]$ is equivalent to $\lambda \vec y.   M[M[u]]$ 
  where $M[u]$ is a hole of type o. This lemma holds only if all constants are
  of type o.

## Mail Andrzeja

1. “atomic matching” jest zdefiniowane jako układ równań, w którym po prawej stronie mogą być tylko stałe typu o. Tzn. taka definicja mówi, że w rozwiązaniach ważny jest “potencjał do produkowania stałych typu o”.

2. Tak się składa, że pojęcie "kontekstowej równoważności" dla lambda-termów jest oparte na testowaniu zbieżności do takich stałych: t1 =ctx= t2 <=> (dla każdego kontekstu C[-]:o i c:o,
(C[t1] ->* c <=> C[t2] ->* c). 

3. Wiadomo, że liczba klas równoważności względem =ctx= jest skończona, więc - żeby rozwiązać “atomic matching” - wystarczy je po kolei sprawdzić. Padovani pokazał, jak można wypisać wszystkiego takie klasy (“listing algorithm”). Jego podejście opiera się na przekształceniach termów do pewnej równoważnej postaci (“cellular”) - Pierre opisuje te przekształcenia w bardziej przystępny sposób niż Padovani.

Dzięki “listing algorithm”, można też rozstrzygnąć, czy dane dwa lambda-termu są =ctx= równoważne: można wypisać wszystkie klasy równoważności dla typów argumentów, po kolei aplikować do nich dane termy i porównać wynik. Nie ma chyba w tej chwili innego algorytmu rozstrzygania takiej równoważności. Wydaje mi się, że problem zostawiony przez Luke’a i Nikosa (tzn. *-REACH(FPCF*, FPCF)) może być jakoś powiązany z powyższymi problemami.

Do ogólnego przypadku “matching”, “kontekstowa równoważność” nie wystarcza, bo trzeba wygenerować więcej niż stałe. Być może można zdefiniować inne pojęcie równoważności, np. testowanie zbieżności do “Church numerals” albo “drzew binarnych", ale nie wiem, czy w czymś pomaga, bo liczba klas równoważności będzie nieskończona.

Tak, jak zauważyłeś, potrzebujemy automatów, które potrafią oszacować aplikacje lambda-termów, ale nie mogą być na tyle silne, żeby można było ich użyć do ewaluacji w modelach skończonych. Model Stirlinga okazał się za mocny, bo mieliśmy dostęp do każdego wiązania - model Marcina/Ranka pozwala się skupić na 1 wiązaniu naraz albo na kilku rozłącznych wiązaniach, ale nie wiem, czy to wystarczy, żeby cokolwiek oszacować.

Być może głębsza analiza struktury “traversals” pozwolala na bardziej oszczędne modelowanie niż u Stirlinga/Onga (“variable profiles”), ale na razie tego nie widzę...

## Redukcja do prostrzych typow

W załączonym rodziale o lambda-rachunku znalazłem Twierdzenie 3.4.8 (Reducibility Theorem), które mówi, że równoważność beta+eta każdego typu da się zredukować do typu T^2 = 1_2 -> o -> o.

O ile dobrze rozszyfrowałem notację (3.4.4), to 1_2 = o -> o -> o, więc

T^2 = (o -> o -> o) -> o -> o,

czyli T^2 to typ drzew binarnych.

Redukowalność oznacza, że dla każdego typu T istnieje term Phi_T: T -> T_2 taki, że M1 =_{beta+eta} M2:T  <=> Phi_T M1 =_{beta+eta} Phi_T M2: T^2.

————

Dzięki temu można przekształcić problem matching 

F X = G : T 

na typ T^2: 

(Phi_T F) X = Phi_T G: T^2.

Teraz aplikując obie strony do stałych br: o -> o -> o i leaf: o, dostajemy

(Phi_T F) X br leaf = Phi_T G br leaf : o,

gdzie prawa strona jest drzewem, np. br (br leaf leaf) leaf: o.

Czyli cały problem redukuje się do

H X = t : o,

gdzie H = (\x. \Phi_T F x br leaf), czyli H jest lambda-termem ze stałymi {br, leaf}, t jest drzewem zbudowanym z {br, leaf}, a X jest nieznanym lambda-termem bez stałych.

[Works/Andrzej/Data-trees/andrzej-notatki]