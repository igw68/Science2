# Leafy automta September 2020

A file with some notes is [/Users/igw/Works/Andrzej/Leafy_Future-28aug]

1. Jest parę uproszczeń które wynikają z własności automatów otrzymanych z translacji termów

	•	Poziomy danych można podzielić na poziomy P oraz na poziomy O. Korzeń ma poziom P.
	•	Poziomy P mogą zmieniać stan, ale poziomy O trzymają tylko stan który miały gdy wierzchołek został stworzony.
  • Poziomy P mają ograniczoną liczbę dzieci: jeśli nie ma while to jest
  ograniczenie na liczbę dzieci w całej rozgrywce. Jeśli jest while to jest
  ograniczenie na liczbę dzieci w każdym stanie. 
	•	Kiedy likwidujemy wierzchołki P to nie musimy sprawdzać czy to jest liść.
	•	To ostatnie spostrzeżenie powoduje, że można uprościć tłumaczenie i nie mieć \e-przejść.
	•	Niestety to nie daje nam jeszcze szans aby złapać równoważność programów automatami, bo mamy kodowanie linków przy pomocy liczb

2. Wygląda na to, że leafy automata gdzie można tylko sprawdzić stan ojca kiedy
   wierzchołek jest likwidowany mają rozstrzygalny problem pustości. 

3. Uwaga 2 daje rozstrzygalność jakiegoś fragmentu, ale trzeba aby zmienne były
   zupełnie lokalne, i bez semaforów.

4. Ciekawy przypadek jest kiedy mamy zmienne i nie mamy semaforów. To wygląda
   trochę na nasz fragment z Helmutem. Co więcej jest nieograniczony spawn bo on
   jest kontrolowany przez otoczenie.  

5. Innym ciekawym przypadkiem może być przypadek bez while. Niestety while da
   się wyprogramować dwoma zmiennymi o zagnieżdżeniu 2. Tak więc trzeba by mieć
   jeszcze jakieś ograniczenie. 


