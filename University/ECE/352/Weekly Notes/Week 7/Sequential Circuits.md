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