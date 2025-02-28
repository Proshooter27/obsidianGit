Represents a decimal number in binary
- We use 4 bits per decimal digit


**Note:** Binary numbers 1010$_2$ to 1111$_2$ cannot be used to represent a decimal digit.

## An Example:
![[Binary Coded Decimal Example.png]]


### Binary Coded Decimal Addition
1. Add each group of 4 bits starting from the right
2. If a group sum $\ge$ 10, subtract 10 to get that digit value and carry over a to the next group.

![[BCD Addition Example.png]]

