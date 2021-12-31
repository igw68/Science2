# Disrtibuted systems at Amazon

[A second conversation with Werner Vogels, CACM march 2021 vol 64 no 3 pp50-]
[dynamo-amazon.pdf]

- They use TLA+ extensively for verification
  
# Principles of distributes system design
- Decentralization: use fully decentralized techniques to remove scaling bottlenecks
- Asynchrony
- Autonomy: individual components can make decisions based on local information
- Local responsibility: each component is responsible for its consistency
- Controlled concurrency: no or limited concurrency control is required
- Failure tolerant: failure of components is normal mode of operation
- Controlled parallelism: abstractions are such that parallelism can be used to
  speed up some tasks
- Decompose intro small well-understood blocks: do not try to provide a single
  service that does everything
- Symmetry: nodes in the system are identical in terms of functionality and
  require no or minimal node-specific configuraiton
- Simplicity