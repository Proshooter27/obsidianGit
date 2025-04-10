It is a selection component that selects a data input value based on the select input value to drive an output.

![[Multiplexers.png]]

### Structure of a Mux:
It generally consists of a decoder (In the below photo, it shows the less abstract version of a decoder) whose outputs are ANDed with the data inputs.

![[Multiplexers-1.png]]

### Logic function of a Mux:
It is the summation of the product of the minterm and its corresponding data input value.

![[Multiplexers-2.png]]

### Another way of building a Mux:
- We can build large muxes using smaller muxes (similar to decoders)

![[Multiplexers-3.png]]

- It is a hierarchical system that gives out the appropriate output.
