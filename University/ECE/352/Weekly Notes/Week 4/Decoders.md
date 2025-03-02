Converts an n-bit input code into a unique m-bit output code
- n $\leq$ m $\leq$ 2<sup>n</sup> 
- **There can be some unused codes**

### Example: A 2:4 Decoder
Only one of the outputs can have a value 1 while the rest of the outputs have a value of 0. This is dictated by the input code.

> Easy way to remember how it works - The input code is a binary number and the output label that has a value same as the input binary number will have an output of 1.

![[Decoders.png]]

### Using minterms to represent SOPs:
Every output label can be used to represent a minterm of a given function.

![[Decoders-1.png]]


### Structure of a decoder:
![[Decoders-2.png]]

In this decoder, if you look at the circuit of the A0 input. It looks like a 1:2 decoder similar like the one below

![[Decoders-3.png]]

Hence, we can say that we can use hierarchy to create a larger decoder from a smaller one.

