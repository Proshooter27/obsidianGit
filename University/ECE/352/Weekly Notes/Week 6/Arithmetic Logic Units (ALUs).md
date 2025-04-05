- An ALU is a structure that can perform multiple different operations.
- It contains sub-circuits for arithmetic operations and sub-circuits for logic operations.
- Uses “mode” inputs to choose the operation; an ALU with N “mode” bits can have up to 2N modes

### Example:
![[Pasted image 20250405180601.png]]

#### Building the ALU,
We use the modes specified in the ISA to value fixed the adder to do the operation that we want to do.
![[Pasted image 20250405180752.png]]

#### Mode Bits:
- Sometimes we need to design an ALU with specific functionality, but have the flexibility to choose our own mode bits
- The Instruction Set Architecture for a processor specifies the encoding of instructions into bits



## Generic ALU Structure:
- All cells get the same mode signals
- Cells have connections to their neighbors for carry, shifts, rotates, etc.
![[Pasted image 20250405181959.png]]

Now, if for example we wanna do a shift right, we then connect the value at A<sub>k</.sub> to the arrow going towards the right bit and value fix the left most arrow that is going right as 0.

> Note:
> 1. Logical Shift Right: Sets the MSB as 0
> 2. Arithmetic Shift Right: Sets the MSB as the same value of the original MSB.
