# Never stop learning

Bertolino, A., Calabr`o, A., Merten, M., Steﬀen, B.: Never-Stop Learning:
Continuous Validation of Learned Models for Evolving Systems through Monitoring.
ERCIM News 2012(88) (2012)

The idea is that instead of a teacher we have monitor that collects traces of
the system. It plays every trace in the current model. Once it gets a trace that
is not in the model, it reports it as counterexample and a new model is formed
via learning.

The problem with this approach is that we only get positive counter-examples
(runs that are indeed runs of the system). Maybe in the paper they say what they
do to get negative examples.
