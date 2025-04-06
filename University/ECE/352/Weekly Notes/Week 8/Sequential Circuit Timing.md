- How fast can we clock a sequential circuit?
![[Pasted image 20250406181908.png]]
- The answer depends on both the flip-flop timing parameters and the delays of combinational logic elements in the circuit
	- Flip-flop output changes must propagate through the circuit to the flip-flop inputs before the next clock edge

#### Minimum Clock Period (t<sub>min</sub>)
- The minimum clock period is the smallest feasible clock period
	- 
	- Need time for a change to get out of a flip-flop, through the circuit, and be present at another flip-flop input before the start of the set-up time
![[Pasted image 20250406183037.png]]
- t<sub>comb</sub> is the longest delay of any path between a flip-flop output and a flip-flop input 
	- We do **NOT** consider paths from circuit inputs

