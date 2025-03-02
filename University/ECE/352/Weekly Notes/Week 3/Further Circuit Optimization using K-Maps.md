### Terminology:
1. **Implicant:** *any* product term(group) where *all* included minterms are 1.
2. **Prime Implicant:** a group that cannot be double in size in any direction without causing it to include a 0.
3. **Essential Prime Implicant:** A prime implicant that is the *only choice* for covering a needed minterm.
4. **Selection Rule:** Each prime implicant in the solution must include at least one minterm *not* included in any other prime implicant in the solution.

### Process of finding the best representation:
1. Find all the prime implicants.
2. Immediately include all the essential PIs.
3. If all 1's are not included:
	1. Eliminate the redundant PIs
	2. Cover remaining uncovers 1's using PI's
4. **Stop when all the 1s are covered.**

## Using K-maps to represent POSs:
There are 2 main methods of doing so:
1. Group all the 0s and write the corresponding sum terms.
	- ![[Further Circuit Optimization using K-Maps.png]]
2. Solve for the complement of the func