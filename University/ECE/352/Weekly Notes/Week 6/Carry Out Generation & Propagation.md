Let us consider a case where we are adding 2 numbers **A** & **B**
### Carry-Out Generation:
If A = 1 & B = 1,
- We can say for sure that C<sub>out</sub> is 1 regardless of C<sub>in</sub>

![[Pasted image 20250405182931.png]]

### Carry-Out Propagation:
If A ≠ B,
- C<sub>out</sub> is equal to C<sub>in</sub>

![[Pasted image 20250405183231.png]]

### There are cases when C<sub>out</sub> has to be 0:
If A = 0 & B = 0,
	C<sub>out</sub> is 0 regardless of C<sub>in</sub>

![[Pasted image 20250405190707.png]]

Now, let us word this function.

C<sub>out</sub> is 1 when the addition generates an carry **or** when the addition propagates **and** the C<sub>in</sub> is 1.
Which is,
- **C<sub>k+1</sub> = G<sub>k</sub> + P<sub>k</sub>C<sub>k</sub>**

#### Now, we can reorganize the full adder by just implementing the above function.

![[Pasted image 20250405192000.png]]

The first **[[Arithmetic Structures#Half Adder|Half Adder]]** does the actual calculation of the addition then next half adder actually calculates the C<sub>out</sub>. So, we can replace the second half adder with a new circuit that implements the above function.

### We can now create a Ripple Carry Adder by using PFAs and a Carry Chain.

![[Pasted image 20250405200447.png]]

### Delays in a Circuit:
- A gate’s output is not actually the result of its logic function until some time after the input(s) change.
- Each gate along a path from a circuit input to a circuit output adds to the delay of that path.
- The path with the longest delay from ANY input to ANY output is called the “**critical path**”

### But, why do we compute the carry differently?
- Ripple carry adders are small and easy to create
- But ripple carry adders are slow!