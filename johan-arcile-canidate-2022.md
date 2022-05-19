# Johan Arcile candidate 2022

## His VerifCar system
- How big models he gets? What does he verify
- What is it about approximation?
- Layered exploration ??
- He has something about diamonds and partial-order

## Multi-agent with periodic timed tasks
- Every agent is acyclic. 
- Periodically each agent is reinitialized if it is in a final location
- every transition has a finite time interval when it can be performed (every
  agent has  one clock that is reset at initialization)
- there may be common variables to agents
- Once again he has a challenge of POR
  - weak and strong variables
- What he calls acceleration is to group together intervals where no new action happens.
- [ ] What is this thing about layers>
- [ ] What is his exploration technique?
- [ ] Why he needs non-blocking (every transition may be fired in the future of
  any reachable state)

## Timed with parameters
- He works in Etienne André system IMITATOR (CAV'21)
- Paper written in "old style", but there are some technical results
- Normally extrapolation depends on maximal constant M. 
- Subclasses where they can show that there is a biggest constant (bigger
  parameteres do not add behaviors). But they have a problem with parameters
  that tend to 0.
- They have union of zones. He does not explain exactly why
- He is interested in our paper "Better abstractions". 
  - inclusion of symbolic not convex state spaces
  - he wants to do the same for liveness

## VerifCar
- network of cyclic timed automata. Reinitialization is at a precise time moment
- variables do not influence system behaviour
- division on layers: first layer is when the whole system goes back to the
  initial state.
- He does not like to have discreete time. He does not want what constraint he
  want to remove. There is some interesting notion of maximal zone.

## Future plans
- extrapolation non-convex in the context of parametric
- complexite assez interesant (tres slopy en description de notre travail)





[2020-10-16-Johan-Arcile]
