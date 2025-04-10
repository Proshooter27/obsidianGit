#### Definitions:
1. Combinational Circuit: Outputs are a function of **only current** circuit inputs
2. Sequential Circuits: Outputs are a function of **not only the current** circuit inputs but also what has happened in the **past**

### Finite State Machines (FSMs)
A sequential circuit that has a **finite** number of possible states
- Limited by the number of flip-flops in the circuit

### Synchronous Sequential Circuits
- Once per clock cycle, the values in the storage elements are updated with the new state information
	- The “next state” becomes the “current state”
- The next state values are produced by a combinational function of the current state values and the circuit inputs
- The circuit outputs are produced by a combinational function of the current state and <u>possibly</u> the circuit inputs

#### Anatomy of a Simple Seq. Circuit
![[Pasted image 20250406160418.png]]

#### Current vs. Next State
 - **Current state** is the set of values that are stored in the FFs at a given time
	 - Remember: FFs output their <u>current</u> values
- **Next state** is the set of values that <u>will be stored</u> into the FFs <u>when they change state</u>

### State Tables
We list the possible states and the possible inputs that can be received for a circuit and the output of the circuit.
![[Pasted image 20250406161250.png]]

![[Pasted image 20250406161335.png]]