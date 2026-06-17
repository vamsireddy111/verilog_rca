# 4-bit Ripple Carry Adder (RCA) using Verilog
# Overview

A Ripple Carry Adder (RCA) is a digital circuit used to perform binary addition of multi-bit numbers. 
It is constructed by cascading multiple Full Adders, where the carry output of one stage becomes the carry input of the next stage.

This project demonstrates the design and simulation of a 4-bit Ripple Carry Adder using Verilog HDL.

# Working Principle

The RCA adds two 4-bit numbers:

A[3:0]
B[3:0]
Cin (initial carry input)
# Outputs:
Sum[3:0]
Cout (final carry output)

# Carry Propagation (Why “Ripple”?)

Carry flows sequentially through each Full Adder:

Cin → FA0 → C1 → FA1 → C2 → FA2 → C3 → FA3 → Cout

Each stage waits for previous carry, causing delay.

# Design Structure
4 × Full Adders
Internal carry wires: C1, C2, C3
Hierarchical design (module reuse)

# Key Observations
Carry propagates sequentially from LSB to MSB
Delay increases with number of bits
Output is correct but not optimized for speed
