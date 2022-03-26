# comp_struc_1d
This repository houses the Lucid files for the 50.004 Computation Structures 1D Project taken in 2022 Spring.

## 16 bit Arithmetic Logic Unit
Takes in two 16 bit inputs and returns one 16 bit output.  
Written in Lucid Hardware Description Language, compiled in Alchitry Labs IDE and Xilinx Vivado.  
2nd hardware deliverable for 50.002 Computation Structures class in 2022 Spring.

### File Description
au_top.luc contains the top level functions that deal with physical IO.  
alu.luc ties together the 16 bit adder, multiplier, compare, boolean and shifter modules.  
alu_tester serves as an interface between the auto and manual testers.  
manual_tester implements manual testing capabilities for the ALU. 
auto_tester connects the tester FSM to the ROM to retrieve test cases and inputs to feed into the ALU.  
alu_fsm defines the FSM that advances to the next test case.  
tester_ROM.luc contains the correct answers for each function. 

## Bop it Game

### File Description
bop_alu_wdsel.luc contains the ALU
bop_controlunit.luc that generates the control signals to support different states of the FSM.
bop_regfile.luc contains the Register File tha
bop_slowclock.luc contains 
