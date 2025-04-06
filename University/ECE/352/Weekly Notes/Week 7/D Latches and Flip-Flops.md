# D-Latches
### How can store data?
We use a D-latch.
![[Pasted image 20250406144842.png]]

When we let the value in D through, it value stored will go round and round to be stored.

>**What happens if there is contention?**
>The bottom inverter is weak, and the [[Tri-states|tristate]] can overpower it without damage.

But, now the question still remains, **when** do we let the Latch take an input value?
We use the [[Clock Signal]]. Whenever we get a positive-edge, we update the value stored in the flip-flop.

# Flip-Flops
- We build a “flip-flop” (FF) by connecting two latches together in Master-Slave organization
- The output of the below flip-flop only changes on the <u>negative edge</u> of the control signal (the clock)
![[Pasted image 20250406150300.png]]

> The purpose of having two D-latches in a flip-flop is to make sure that we save a value at only the positive-edge.
> 
> When the clock has a Positive-Edge, the Master Latch lets a value through and stores it and when the cock has a Negative-Edge, the Slave Latch stores the value that the Master Latch has and makes sure that it will save the correct value at that was at the positive-edge.

### Timing Waveforms
In reality, there is some delay after the active clock edge before the FF input is stored and appears at the FF output.
![[Pasted image 20250406153041.png]]

