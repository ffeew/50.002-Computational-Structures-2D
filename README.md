# 50.002-Computational-Structures-2D

## Project Description
The goal of this design project is to improve the performance of the 32-bit adder/subtractor
unit you built as part of Lab #3:

## Solution
### Structure of Adder
We used the 32-bit Kogge Stone Adder (KSA) architecture with some amendments. We added an
additional lane for the carry-in (ALUFN0) to allow for the addition of signed integers. We also
buffered the ALUFN0 signal via a tree format to optimise the delay and chip area both within the
KSA and for the 1’s complement of input B aiming to maintain at most 1:4 connection. The KSA
design minimises the fan-out for each level of output, creating a minimised dependency on a singular
output gate. This will increase the processing speed through the use of parallel processing of inputs to
minimise the propagation delay.

The fastest timing the adder can pass is 3ns. (The propagation delay of the 32-bit adder is 2.1531ns)
