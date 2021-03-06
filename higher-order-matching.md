# Higher-order matching

* Literature is in [[higher-order-martching-papers]]

- [[lambda-definability]]
- [[well-quasi-orderings]]
- Maybe alternating visibly pushdown automata on trees can help [[visibly-pushdown-automata]]


Nice simple approach of Parys [[a-reduction-approach-to-homc]]

# TODO
Spisac notatke z Dagstuh z prosta definicja automatu. Z \theta alternacja
Napisac dowod nierozstrzygalnosci tych automatow. 2 liczniki. Uzyc alternacji
aby przekazac stan tak wiec nie automat bedzie monotoniczny.
Zobaczyc gdzie jest miejsce na rozstrzygalnosc.
Jaka jest zlozonosc dla przypadku z 1 atomem?

# 2022-04-11
Jesli bysmy chcieli robic Joly nierozstrzygalnosc na automatach to trzeba isc do
dosyc wysokich typow. 

Saturacja: 
Zlozenie rownolegle wymaga produktu (aby zrobic interleaving)
Byc moze tlumaczenie Algola na automaty moze byc liniowe.
Chcemy miec model ktory autmatycznie generuje ciagi ktore spelniaja saturacje.
Mamy tez nadzieje ze tlumaczenie z automatow do Algola bedzie prostrze
[Plik z overleaf]





# 2022-03-28
Andrzej czytal Joly. Ale jego dowody maja dziury.
Model monotoniczny nad 1-nym elementem moze miec definiowalnosc
nierozstrzygalna.
Jego podejscie jest wykrywanie czy term jest napompowany. 
To robi przez danie specjalnych argumentow termowi.
Zapropragowac OK przy pomocy automatow.

# 2022-03-21
Definiowalnosc na modelami z 2 elementami
Nierozstrzygalnosc gdy jest ustalony typ ale zmienia sie ilosc elementow w modelu
Nierozstrzygalnosc gdy model jest ustalony ale zmienia sie typy.
Typ L : ((o->o)->o) -> (o->o->o)->o ->o

Game semantics on one slide

![picture 8](images/2d37f695c2f647d8c8697ff6b7a9c43b1b775b466801a50f3ccf7467598a1c10.png)  


# 2022-03-15
Zrobic przypadek atomowy przy pomocy automatow.
Podprzypadek jest czy typ jest zamieszkaly w teorii intuicjonistycznej
(wystarczy 1 zmienna kazdego typu).
Padovani potrzebuje tylko 2 atomow, ale w profilach wystarczy uzywac 1 stalej,
bo mozemy zalozyc, ze po prawej stronie mamy zawsze ten sam atom.

# 2022-03-02

# 2022-02-16
Harmer nie przechodzi przez automaty bo zapomnielismy o y na samej gorze.
Pytanie: Czy mozna zrobic Padovaniego przez automaty.
Wyglada na to, ze Harmer przechodzi uzywajac argumentu Padovaniego.
Czy mozna udowodnic Hamera automatami?

# 2022-01-24
Monotonicity probably gives decidability for Stirling automata of order 5. 
May it be the case that monotonicity is sufficient condition for decidability?
A hypothesis is that it does not help for order 6.

## 2021-12-01
Comon Jurski []

## [[2021-11-16]]
Dany profil nad jednym atomem sprawdzic czy isntieje term o tym profilu. To
wydaje sie rownowazne pustosci automatow nad postaciami Harmera wiec chyba
roztrzygalne.


## [[2021-23-08]]
Praca Russ Harmer o komorkowych termach. To uzywa niewinnosci.
Trzeba ograniczyc liczbe precinajacych sie lambda, to odpowiada liczbie
otwartych zmiennych. 
Przypadek posredni: jak interpolacja atomowa, ale stale z prawej strony maja
wyzszy typ.
Jak liczba otwartych zmiennych jest widoczna w higher-order pushdown automaton? 
To widac w stanie bo uzywamy zmiennych w stanie, a zmienne moga tez byc
zmiennymi zwiazanymi.
Moze jeszcze lepiej jest uzywac automatu z drzewiastymi stosami z pracy z Lorenzo?

## [[2021-08-02]] Zoom z Andrzejem
* Jest prosty dow??d na to ze automaty Stirlinga s?? nieroztrzygalne. Alternacja w
  jego wersji pozwala na zaznaczanie kazdej lambdy. To sie dzieje dzieki temu,
  ze jego automat bedac w zmiennej, moze spojzec na stan w lambda ktora ja
  wiaze.
* Automaty z jednym rejestrem Marcina i Ranko w pewnwym sensie s?? bardzo podobne
  ale nie mog??  patrzec na stan automatu w lambdzie. Przez to sa one
  rozstrzygalne. 
* Powinnism spojzec na prostrzy problem fx=a gdzie a jest jedna stala typu 0.
  Rozstrzygalnosc tego problemu jest prostrza, ale moze nam si?? uda znalezc
  automat ktory opisuje wszystkie rozwiazania. Sa dwie prace na ten temat. 
  Padowani i Clairambault w katalogu [Works/Andrzej/Data Treee Automata]
* [[atomic-higher-order-matching]]

Joly m??wi o paru zwi??zkach mi??dzy higher-order matching i problamach
definiwalno??ci.
[joly-loader-undecidability.pdf]
For example HOM for beta instead of beta-eta quality is undecidable. 

* Wydaje sie, ze automaty Stirlinga sa specjalna wersja class automata. Z drugiej
strony latwiej jest pracowac z register automata. Czy nie ma jakies translacji z
jedngo w drugie?
* Profile potrzebne do matching wydaja sie specjalne. 
  Ogolnie pustosc alternujacych automatow Stirlinga jest nierostrzygalna. To
  wynik z zakodowania Loadera. Wydaje sie jednak, ze do matching profile sa
  jakies specjalen
- [ ] Spojzec na dowod Loadera i starac sie zrozumiec roznice.
* (Z jakis powodow unarny PCF jest rozstrzygalny)
- [ ] Zobaczyc dowod Joly nierozstrzygalnosci, jest prostrzy niz Loader
  * [joly-loader-undecidability.pdf] w PDF Expert
- [ ] Barendregt ma przetrawione wyniki Loadera


## Mail Andrzeja
Po naszej rozmowie w poniedzia??ek odnalaz??em pliki z r????nymi eksperymentami w Haskellu sprzed lat, gdzie testowa??em, jak dzia??a funkcja, kt??ra wykrywa, czy dany term typu Monster reprezentuje kolejk?? (za????czam plik jol.hs).

Funkcja nazywa si?? ???qtest??? i polega na zaaplikowaniu termu do sprytnie dobranej funkcji, kt??ra w pewnym sensie weryfikuje indukcyjnie, czy dany term ma dobr?? struktur??, tzn. 

- ka??de wi??zanie  \f jest u??yte dok??adnie raz,
- je??li \f1 pojawia si?? w termie przed \f2 to aplikacja f1 pojawi si?? przed aplikacj?? f2 (FIFO).

Og??lnie, oznacza to, ??e termy M reprezentuj??ce kolejki mo??na wy??apa?? za pomoc?? r??wnania "M f 1 = 1", gdzie f jest odpowiedni?? funkcj??.

Takich term??w M mo??na potem u??y?? do symulacji automat??w z kolejk?? (queue machines) i sprawdza??, czy si?? zatrzymuj??, aplikuj??c M do kolejnej ???odpowiednio dobranej??? funkcji, kt??ra zale??y od funkcji przej??cia automatu.
Wtedy zatrzymanie maszyny mo??na wyrazi?? przez "M g 0 = 1", gdzie g jest pewn?? funkcj??, kt??ra zale??y od funkcji przej??cia.

Podsumowuj??c, problem stopu dla ???queue machines" redukuje si?? do pytania, czy istnieje term M typu Monster taki, ??e

M f 1 = 1, 
M g 0 = 1.

Gdyby lambda-definiowalno???? by??a rozstrzygalna, mo??na by teraz rozwi??za?? problem stopu.

Powy??szy wyw??d opiera si?? na technikach Joly???ego, ale jego dow??d wydaje mi si?? bardziej skomplikowany, bo symuluje maszyny 2-licznikowe termami typu Monster, a do reprezentowania par ???dec - inc??? u??ywa term??w, kt??re maj?? struktur?? kolejki. Skoro i tak u??ywa term??w ???kolejkowych???, to mo??na ich u??y?? od razu do symulowania maszyn z kolejk?? bez przechodzenia przez maszyny z licznikami. Dow??d Joly???ego jest za to troch?? bardziej ambitny, bo on oba warunki sprawdza naraz i dostaje tylko jedno r??wnanie.

Nie bardzo rozumiem, co z tego wszystkiego wynika dla naszego problemu. Wa??n?? cech?? funkcji f i g jest to, ??e NIE s?? definiowalne w lambda-rachunku (bo patrz?? na argumenty), a w problemie matching wszystko musi by?? lambda-termem. Nie bardzo wiem, jak to uchwyci?? za pomoc?? automatu??? Wygl??da na to, ??e powinien mie?? ograniczon?? mo??liwo???? zmiany stanu, ??eby nie m??g?? dokona?? ewaluacji dowolnych funkcji sko??czonych, ale ??eby jako?? ci??gle m??g?? sobie poradzi?? z matching?

Dla pami??ci, spisa??em poni??ej wszystkie pytania, na kt??re warto by znale???? odpowiedzi z punktu widzenia automat??w.

- Dlaczego ???higher-order matching??? jest rozstrzygalne?
- Dlaczego "unary PCF" jest rozstrzygalne a "binary PCF" nie jest?
- Dlaczego "bot-REACH??? ma niewyja??niony status a ???t-REACH??? jest nierozstrzygalne?


#Andrzej