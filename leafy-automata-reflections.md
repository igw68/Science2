# Leafy automata: reflections

* The intention is that an automaton reads plays where links are encoded as data values.
* Since automaton can either create or destroy a node, every data value is read
  at most twice. On an accepted trace every value is read exactly twice. (not
  really, it may be red when handling lower data values)
* Emptiness of 2-automata is undecidable as we can implement 0-tests, inc, dec
* Emptiness of 1-automata is decidable, but it as VAS it can see if a counter is
  positive, and at the end it checks that all counters are 0. 

- [ ] Can an automaton be deterministic. Where we need non-determinism?
- [ ] New restrictions on the shape of automata may imply that on some levels we
  do not use data values.

	