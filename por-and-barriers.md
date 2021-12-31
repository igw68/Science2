# POR and barriers
date: [[2021-06-10]]
This is about
[BAM: Effcient Model Checking for Barriers, Vafeiadis, V, NETSYS'21]
[vefaiadis-netys2021-barriers.pdf]


* Barrier is a construct that makes all the processes wait at some point. 
  Once they are all there, all of them can proceed.
  The particularity is that the order at which processes arrive at a barrier do
  does not make a difference

## Why there is a problem
The standard conflict relation is: two actions access to the same variable, one
of them is a write. 
A standard implementation of a barrier is a variable decreased by every process.
So when a process arrives at a barrier it is a write. Then there is a read for
0.

## What they do in the paper
They propose a specific independence relation in the framework of weak memory
models and show that it gives exponential gains.

## How to solve the problem with transition systems
Make the barrier process read arrival of other processes in pre-established
order. This avoids exponential explosion for arrival at the barrier. Then we can


#partial-order