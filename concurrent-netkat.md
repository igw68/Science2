# Concurrent NetKAT
Alexandra Silva
#seminar 2021-10-19

Network behavior, there are global variables that packets/routers can examine.
You would like check for absence of loops (or detect loops).
Here they have multiple packets.

NetKAT: Kleene algebra with tests
Tests are testing if a field has a certain value (field=val)
She can assign values to fields
There is also an action of duplication of a packet

NOdes are called ports. Then we specify what happens on links between
components.
(sw=3)(type=SSH)(sw:=5) moves packet SSH from switch 3 to switch 5.

Switch forwarding tables are of this form.
The whole behavior is one itration of a big "if" state.

The semantics is on sequence of packets. Dup, duplicates the first element.
So a program just creates a list of snapshots done with dup

They have a complete axiomatization of Kat by adding axiomatization of
read/write.

They do verification using program equivalence.

Problem: adding concurency to KAT [Kozen et al, 2018] [Hoeare, Moeller et al 09]
exchange law: (e||g)(f||h) <= (ef)||(gh)
This is supposed to capture true concurrency.
The system proposed was inconsistent.

[Begstra & Ponse'11] The main issue is that conjuction is not the same as
testing to conjucts sequentially (in between the value can change).

They have new algebra that is sound (how do they prove this?)[FOSSACS'20]

Now semantics takes a set of packets, and it gives a set of pairs (pomset
recording changes in a global store ,set of packets)







