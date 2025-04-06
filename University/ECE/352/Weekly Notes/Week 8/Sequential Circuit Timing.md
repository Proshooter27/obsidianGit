- How fast can we clock a sequential circuit?
![[Pasted image 20250406181908.png]]
- The answer depends on both the flip-flop timing parameters and the delays of combinational logic elements in the circuit
	- Flip-flop output changes must propagate through the circuit to the flip-flop inputs before the next clock edge

#### Minimum Clock Period (t<sub>min</sub>)
- The minimum clock period is the smallest feasible clock period
	- **t<sub>min</sub> = t<sub>pd</sub> + t<sub>comb</sub> + t<sub>s</sub>**
	- Need time for a change to get out of a flip-flop, through the circuit, and be present at another flip-flop input before the start of the set-up time
![[Pasted image 20250406183037.png]]
- t<sub>comb</sub> is the longest delay of any path between a flip-flop output and a flip-flop input 
	- We do **NOT** consider paths from circuit inputs

#### Slack (t<sub>slack</sub>)
- The difference between actual clock period (tp) and minimum clock period
	- **t<sub>slack</sub> = t<sub>p</sub> - t<sub>min</sub>**
![[Pasted image 20250406183311.png]]
- How should we interpret slack values?
	- **Positive**: could run the circuit faster (don’t have to!)
	- **Negative**: trying to run the circuit too fast
	- **Zero**: running the circuit as fast as it can go
		- Probably not a good idea… just in case…

#### Clock Frequency
- The <u>clock speed</u> of the sequential circuit
	- Faster clock → higher frequency
- <u>Maximum</u> circuit frequency:  f<sub>max</sub> = 1 / t<sub>min</sub>
- <u>Actual</u> circuit frequency:  f = 1 / t<sub>p</sub>

- Remember:
	- Clock period is ps, ns, µs, ms, s…
	- Frequency is Hz, kHz, MHz, GHz…

#### Critical Path
- Longest (largest-delay) path that **begins and ends at a flip-flop** 
	- Can begin and end at the **same** FF!
	- **Only** the paths that begin and end at a flip-flop
		- **Not** looking at the path(s) from the <u>circuit</u> input(s)
![[Pasted image 20250406183822.png]]

