# Addition and Subtraction
### Half Adder:
- [[Half Adder]]

### Full Adder:
- Adds three single-bit inputs where, 2 are the bits from numbers that you are adding and the 3<sup>rd</sup> is Carry-in.
- ![[Arithmetic Structures-1.png]]

### Ripple Carry Adder (RCA):
- Its a series of full adders that carry-overs the overflow of every bit.
- ![[Arithmetic Structures-2.png]]

### Binary Subtractor
- We modify a RCA to do a (A+(-B))
- ![[Arithmetic Structures-3.png]]

### Binary Adder-Subtractor
- It uses an XOR to check whether it is a subtraction or not
- If SUB = 1 then subtraction else addition.
- ![[Arithmetic Structures-4.png]]

### Overflow detection
- Unsigned overflow if **C = 1**
- Signed overflow if **V = 1**
- ![[Arithmetic Structures-5.png]]

# Contraction and Specialized Structures
### Contraction:
- If an input to a circuit will always be a constant value, we can simplify the circuit using the following rules:
![[Pasted image 20250405174007.png]]

#### Example: Incrementer
We use a RCA to do this.
![[Pasted image 20250405174312.png]]

Looking at the LSB,
![[Pasted image 20250405175505.png]]
Middle Bit,
![[Pasted image 20250405175536.png]]
MSB,
![[Pasted image 20250405175555.png]]


So finally the circuit becomes: 
![[Pasted image 20250405175641.png]]