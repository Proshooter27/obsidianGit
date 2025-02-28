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

### There are two types of representations:
1. [[Minterms]]
2. [[Maxterms]
