### How can store data?
We use a D-latch.
![[Pasted image 20250406144842.png]]

When we let the value in D through, it value stored will go round and round to be stored.

>**What happens if there is contention?**
>The bottom inverter is weak, and the [[Tri-states|tristate]] can overpower it without damage.

But, now the question still remains, **when** do we let the Latch take an input value?
We use the [[Clock Signal]]. Whenever we get a positive-edge, we update the value stored in the flip-flop.