# 50.002 Computation Structures: Electronic Game Design
This repository houses the Lucid files for the 50.002 Computation Structures 1D Project taken in 2022 Spring.

## `alu_16bit` 16 bit Arithmetic Logic Unit
Takes in two 16 bit inputs and returns one 16 bit output.  
Written in Lucid Hardware Description Language, compiled in Alchitry Labs IDE and Xilinx Vivado.  
2nd hardware deliverable for 50.002 Computation Structures class in 2022 Spring.

### File Description
`au_top.luc` contains the top level functions that deal with physical IO.  
`alu.luc` ties together the 16 bit adder, multiplier, compare, boolean and shifter modules.  
`alu_tester` serves as an interface between the auto and manual testers.  
`manual_tester` implements manual testing capabilities for the ALU. 
`auto_tester` connects the tester FSM to the ROM to retrieve test cases and inputs to feed into the ALU.  
`alu_fsm` defines the FSM that advances to the next test case.  
`tester_ROM.luc` contains the correct answers for each function. 

## `bit_op` Bit Op! Game

### File Description
`bop_alu_wdsel.luc` contains the ALU and selector muxes
`bop_controlunit.luc` generates the control signals to support different states of the FSM.
`bop_regfile.luc` defines the Register File that reads/writes data during gameplay.
`bop_slwclk_rng.luc` contains the slow clock and RNG modules that generate a slower clock signal and random action signals during gameplay. 
