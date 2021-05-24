# Leafy Automata 5 Oct 2020

- [ ] Is there some part of the automaton that can be deterministic?
- [ ] Understand more complicated restrictions.
  - Rzad parzystych jest ograniczony: wypuszcza tylko ograniczona liczba dzieci w calej historii
    - Jest ograniczona liczba momentow kiedy wierzcholek zmienia cos u gory.
    - Mozemy zapomniec, ze stan na poziomach nieparzystych  sie nie zmienia.
- What Algol fragment compiles to decidable automata.
  - Tylko aplikacja zmienia glebokośc
  - Odleglosc daje mozliwosc skompilowania new X in f(x:=3)
  - Czy mozemy symulowac dowolna glebokosc?
    - newvar x:=0 in f(newvar y in f(y:=1|| x:=!y)) wydaje sie ze mozna
      przekawartosc wyzej ale nie ma while co powoduje, ze nie mozemy miec
      niograniczenie wiele zmian.

- Zapuscic tester rownolegle. Czy mozemy miec wolne zmiene dowolnie gleboko?
- [ ] Dowod Tw 3 w app E

#Andrzej