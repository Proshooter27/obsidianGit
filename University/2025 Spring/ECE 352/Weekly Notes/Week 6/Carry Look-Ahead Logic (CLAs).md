When we make a CLA, we trade of area/power to get a faster speed.

Each carry bit is a **multi-level** function of the generates and propagates of the lower positions
![[Pasted image 20250406141436.png]]
![[Pasted image 20250406141544.png]]

We can now convert the above Ripple-Carry Adder by opening up the parenthesis.
![[Pasted image 20250406142032.png]]
![[Pasted image 20250406142045.png]]

Now, the **“Flatten”** the ripple-carry equation equates to 2-levels of logic for every C<sub>out</sub>.


### Extending the idea of CLAs
We can't always keep on extending the chain every time we need more bits. So, to solve that issue we pair the CLAs into 4-bit look-ahead blocks.

#### Example: A 16-bit Carry Look-Ahead Adder
![[Pasted image 20250406143803.png]]

Now, the equation looks like the below.
![[Pasted image 20250406144250.png]]

