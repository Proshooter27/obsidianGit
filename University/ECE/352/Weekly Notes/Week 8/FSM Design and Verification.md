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
	- A=0 doesn’t start a pattern
	- A=1 starts a pattern
3. State “1”
	- A=0 ruins pattern: start over
	- A=1 continues pattern
4. State “11”
	- A=0 completes pattern; start over for next
	- A=1 holds place in pattern

>Mealy needs fewer states than Moore for similar functionality.
>Remember, the functionality is not the same

### Examples:
- Used meaningful names to help us build diagram
- Now need to pick binary state encoding
	- Doesn’t have to be Gray code, but it works well here

#### Lets design a Moore Machine:
![[Pasted image 20250406175958.png]]

#### Lets design a Mealy Machine:
![[Pasted image 20250406180037.png]]

Now, we have to implement these functions in a circuit.
![[Pasted image 20250406180125.png]]

### Verification:
- We have to make sure that the circuit matches the original specifications.
	- Exhaustive testing is only practical for smaller circuits, and cannot test all possible sequences
	- Instead test each transition and output, with a minimum set of input vectors (minimum  check correctness with less effort)
		- Get to each state using reset and/or a sequence of inputs
		- Leave each state using all possible input combinations (2#inputs)
	- Verify against both specification and state diagram
		- Don’t just verify against equations in case they are incorrect

#### Example:
Create input sequence to test Mealy version of pattern recognizer
![[Pasted image 20250406180554.png]]
