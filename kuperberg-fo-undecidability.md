# Kuperberg-FO-undecidability

## Positive FOL on words
Letters are predicates. More than one predicate can hold at some position
The languages defined in FOpos are monotonic.

- there is a language that is FO definable and monotone, but not definable in FOpos.
  The atomic predicates are a,b,c. a^ is any label containing a.
	L = (a^v^c^)*\cup A^*(abc)A^*
  So for words that do not have (abc) in some position we should have a on
  position 3k, b on 3k+1, c on 3k+2
	Why it is not in FOpos? He uses EF game.
	For FOpos, the letter in u should be included in the letter in v.
  He takes u=(abc)* for v it is ambigues word [(ab)(bc)(ca)]^* but for the last
  letter. This is because beginning and end of the word look like matching u.
	Duplicator matches either with the top part or with the bottom part. 

- Lyndon's theorem: If FO formula defines a positive property then it is
  equivalent to a formula without negation. 
- The theorem is not true for finite structures. [Ajtai, Gurevich, 87] [Stolbushkin'95]
- This conuterexample shows the same result much easier

- Undecidabilty of FOpos.
  Reduction to mortality of TMs: is there a uniform bound on the length of the
  runs from any confifuration.
	This is equivalent to asking if TM has an infinite run [Hoopr'1996]

- L is FOpos definable iff M is mortal.
- He writes configurations in three different way. (u1,u2) if there is a
  transition u1 -> u2 in M. This we can write with a regular condition on two
  coordinates.
- L=(C^1C^2C^3)^*
- u does not encode the runs
- If M is not mortal: u u_1 u_2 .. u_n very long run. v is (u1u2)(u2u3)..(u_{n-1}un)
  we show in the same way that L is not FO^+ definable
- If M is mortal wiht bound n. He uses the lengths of the play. Spoiler wins in
  2n rounds.





#seminar 2021-28-09