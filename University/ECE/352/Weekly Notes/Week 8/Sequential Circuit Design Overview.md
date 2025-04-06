### Sequential Circuit Design
1. **Specification:** 
	- Defines what the circuit must do
	- Specifies the input and output signals, and the meaning of each
	- In reality, there will also be numerous additional constraints related to timing, power, energy, environmental conditions, semiconductor technology, and interoperability with other parts of the overall design
2. **State diagram and state table:**
	- What states are required?
	- In each state, what should the circuit do next?
	- Validate the state diagram by testing it under various input scenarios
	- Usually, we first draw a state diagram to graphically define the behavior of the circuit, and then create a state table from the state diagram
3. **Optimization:**
	- Optimize the state machine, including merging states where possible 
	- Determine behavior in any unused states
4. **State assignment:**
	- Determine the required number of flip-flops 
	- Assign binary values to each state
5. **Combinational logic design:**
	- Use the state table data to determine the optimal combinational logic required for.
		- Next-state logic (drives flip-flop inputs)
		- Circuit output logic
6. **Implementation:**
	- Create the circuit’s schematic diagram by placing the flip-flops and the required combinational logic
7. **Verification:**
	- Create a test vector that exercises the machine such that each state transition is tested
	- Test that the state transitions and output(s) match the state diagram
	- Verify that the machine’s behavior meets the original specification