As an example we will look at an example that outputs a 1 whenever the circuit recognizes a sequence of “110” within a serial bit pattern
### Designing a Moore Machine:
1. Need to start somewhere…
	- Start with Reset state!
	- Haven’t seen a useful part of the pattern yet…
2. State “Nada” (“Nothing”)
	- A=0 doesn’t start a pattern
	- A=1 starts a pattern
3. State “1”
	- A=0 ruins pattern: start over
	- A=1 continues the pattern
4. State “11”
	- A=0 completes the pattern
	- A=1 neither continues nor ruins pattern (still have “11”)
5. State “110”
	- A=0: start over…
	- A=1: start over with first 1

![[Pasted image 20250406165513.png]]

### Designing a Mealy Machine:
1. Start with the reset…
2. State “Nada”
A=0 doesn’t start a pattern
A=1 starts a pattern
3. State “1”
A=0 ruins pattern: start over
A=1 continues pattern
4. State “11”
A=0 completes pattern; start over for next
A=1 holds place in pattern

- Mealy needs fewer states than Moore for similar functionality
- Remember, the functionality is not the same