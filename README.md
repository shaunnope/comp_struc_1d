# comp_struc_1d

16 bit Arithmetic Logic Unit. Takes in two 16 bit inputs and returns one single bit output.  
Written in Lucid Hardware Description Language, compiled in Alchitry Labs IDE and Xilinx Vivado.  
2nd hardware deliverable for 50002 Computation Structures class in 2022 Spring.

## Description of each file
au_top.luc contains the top level functions that deal with physical IO.  
alu.luc ties together the 16 bit adder, compare, boole and shifter.  
tester_ROM.luc contains the correct answers for each function.  
alu_tester contains the FSM that advances to each state and the corresponding error.  

more functionality to be added.  
