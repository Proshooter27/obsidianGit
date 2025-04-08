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

##### An Example:
Find t<sub>min</sub>, given the following delays (in ns):
![[Pasted image 20250406184602.png]]

> Critical Path Pitfall
> 1. Input paths should NOT be considered when computing f<sub>max</sub> = 1/t<sub>min</sub>
> 	 We only care about FF→FF delays

### Hold Time Violations
- Hold time can be violated if a change at a flip-flop output can propagate through the circuit to a flip-flop input before the end of the hold time
	- Can occur if t<sub>h</sub> > t<sub>pd</sub> + t<sub>comb,min</sub>
	- Need to consider only the fastest (least delay) path from flip-flop output to flip-flop input
- Most flip-flops are now designed so t<sub>h</sub> < t<sub>pd</sub>
	- In that case, hold time cannot be violated even when a flip-flop output is directly connected to a flip-flop input

### Synchronization
- Changes on the circuit’s external inputs could cause violations of the flip-flop set-up and hold times.
- The real problem is that the timing of the input signals is not related to the timing of our clock signal. To fix this, we can “synchronize” those signals such that their changes arrive to our circuit right after the active clock edges.

#### Synchronization Problem:
![[Pasted image 20250408015805.png]]
In this example FSM with two flip-flops, input A determines the next state: 0 if A=0, and 3 if A=1. A changes from 0 to 1 just 5ns before the clock edge. Due to differing delays, the change reaches the top flip-flop in time but not the bottom one. As a result, at the clock edge, the flip-flops capture different inputs and the FSM incorrectly transitions to state 2 instead of 0 or 3.

To prevent timing issues from input changes, we add a flip-flop to synchronize inputs. This ensures input values only change at clock edges. However, it adds delay paths that can affect the minimum clock period (t<sub>min</sub>), potentially requiring a slower clock.

![[Pasted image 20250408020301.png]]

This fixes most input timing problems—except one special case.

Even with synchronization, input changes can violate setup/hold times, possibly causing **metastability**—where the flip-flop output becomes unstable or unpredictable for a short time. Though rare, it can happen. To minimize its effect, we use **multiple flip-flops in a chain**, greatly reducing the chance that metastability propagates. While the risk can't be eliminated entirely, it can be made negligible.

Asynchronous issues can also occur if synchronous design rules are broken. A common mistake is misusing flip-flop **asynchronous inputs** (like preset or clear) for anything other than reset—this bypasses the clock and causes unreliable behavior. Sticking to synchronous design principles helps ensure circuits work reliably and are easier to design.