- A flip-flop only behaves the way we expect it to if we make sure that its synchronous inputs do not change too close to the clock edge
	- If a synchronous input changes too close to the clock edge, the correct value may not be stored!

- The output of a flip-flop will not update instantaneously at the active clock – there will be a delay before Q is known to be correct
- We need to ensure that our clock frequency is not too fast for the design of our circuit
	- A newly-stored value must propagate through its FF and any combinational logic on the way to the next FF, and arrive “early” enough before the next clock edge

> **We need to know:**
> 1. When do values need to get to the FF?
> 2. How long do they need to stay after the edge?
> 3. How long for them to propagate through the FF?
> 4. How long is the path between flip-flops?


#### Flip-Flop Setup Time (t<sub>s</sub>)
Synchronous flip-flop inputs must be stable for a certain time <u>before</u> each active clock edge
![[Pasted image 20250406180911.png]]

#### Flip-Flop Hold Time (t<sub>h</sub>)
Synchronous flip-flop inputs must be stable for a certain time <u>after</u> each active clock edge
![[Pasted image 20250406180939.png]]

#### Flip-Flop Propagation Delay (t<sub>pd</sub>)
The flip-flop output will not reflect the new stored value until some time <u>after</u> the active clock edge
![[Pasted image 20250406181015.png]]

### Flip-Flop Timing Parameters
![[Pasted image 20250406181339.png]]


- Setup (t<sub>s</sub>) and hold (t<sub>h</sub>) times: 
	- Changes to FF input during these times may or may not be reflected in the stored value…
	- DO NOT change the FF input values during these times
	- This also means you should not have the circuit inputs change on active clock edges when simulating a circuit!
- Propagation delay (t<sub>pd</sub>)
	- Takes some time after the clock edge for the stored FF value to “show up” at outputs
- Clock period
	- Clock can only go so fast and still have the FFs behave in an expected manner due to the above