We usually consider 2 output states 0 and 1. But we also use another type of output called **High Impedance(hi-Z)** 
- It is denoted as Z and it is neither a 0 or 1.

A **Tri-State Buffer** is a component that allows a input to pass if enabled otherwise, it is an *open* circuit.

![[Tri-states.png]]![[Tri-states-1.png]]
### Using Tri-State Buffers:
![[Tri-states-2.png]]

> A Circuit must always have a valid output, be it 0 or 1.

### Implementing Logic with Tristates:

![[Tri-states-3.png]]
![[Tri-states-4.png]]

## Circuits that you should NEVER make:
1. ![[Tri-states-5.png]]
2. ![[Tri-states-6.png]]
3. ![[Tri-states-7.png]]
4. ![[Tri-states-8.png]]
5. ![[Tri-states-9.png]]

## Things you SHOULD do:
1. Make sure *every* gate input is driven by a valid logi