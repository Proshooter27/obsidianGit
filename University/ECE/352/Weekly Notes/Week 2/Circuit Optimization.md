A circuit is call *"n-level"* if the **longest** path from any input to output goes through *n gates*.

> In this course we'll general try to get the optimal 2-level implementation of circuits

There are usually 2 types of 2-level circuits:
1. **Sum Of Products(SOPs)**:
	- AND --> OR
	- F = AB + BC + D
	- ![[SOP.png]]
2. **Product Of Sums(POSs)**:
	- OR --> AND
	- G = W(X+Y)(Y+Z)
	- ![[POS.png]]

### There are two types of representations of circuits:
1. [[Minterms]]
	- When looking at these, we associate it with an **OR** of **1s**
2. [[Maxterms]]
	- When looking at these, we associate it with an **AND** of **0s**


#### Converting between Minterms and Maxterms:
We just use De Morgan's Law from [[Basic Boolean Identities]]

![[Conversion.png]]


# Multi-level Circuit Opti
