# Reasoning about threads with locks

[kahlon2005_reasoningAboutLocks.pdf]
#distributed
They say that nested locks is a commonly occurring case.
In certain programming languages like Java and C# locks are syntactically
guaranteed to be nested.
Without restriction, even for two threads, programs with locks have undecidable
reachability problem (when threads are pushdowns).

It looks that they cheat a little bit, because they talk about reaching "exists
run reaching 2 given positions in 2 processes". This allows to look only at the
two processes in question because the other processes can at most block the two.

It is much more difficult to decide if no run arrives at a global deadlock. Here
we need to consider all the processes. 