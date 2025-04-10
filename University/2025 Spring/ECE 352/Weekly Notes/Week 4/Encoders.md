- Performs the reverse operation of a decoder.
- Takes up to 2<sup>n</sup> inputs and produces s n-bit output

![[Encoders.png]]

> However, if you have Multiple 1 bit inputs or zero 1 bit inputs, it would give you an erroneous output value. That's where **priority encoders** come into the picture

## Priority Encoders
It resolves the issue by assigning each bit a priority.

![[Encoders-1.png]]

> It always prioritizes 1s at higher-numbered positions.
> That means whatever is the highest-numbered label that has a value 1, it gets represented in a binary number as an output of an encoder.

> **Now, what if all the values are zero?**

#### We solve this by using a Value Detect system.

Whenever all the inputs become 0, that means the value of V becomes 0 making all the other outputs as Don't Cares.

However if at-least one input is 1, then the value of V becomes 1 making the encoder work as normal.

![[Encoders-2.png]]

