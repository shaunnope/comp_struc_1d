# 50.002 Computation Structures: Electronic Game Design
This repository houses the Lucid files for the 50.002 Computation Structures 1D Project taken in 2022 Spring.

Foo Chuan Shao 1005549
Emmanuel J Lopez 1005407
Koh Jia Jun 1005453
Jolin Teo Hui Lyn 1005344
Joshua Ng Tze Wee 1005285
Yap Zhan Hao, Sean	1005153
Varshini Harthachtiramalogan 1005185
Wang Zhao 1005460


## `bit_op` Bit Op! Game

Bit Op! is a single player game inspired by Bop It by Hasbro.  

<img src="https://github.com/shaunnope/comp_struct_1d/blob/master/images/bitop_device.png" width="200">

A video on how Bit Op! is played is available here.
<img src="https://github.com/shaunnope/comp_struct_1d/blob/master/images/bitop_thumbnail.png" width="100">  
[link text](https://youtu.be/HqunbQNz37w "Bit Op! Video")


### `bit_op` Bit Op! Game Description
With 3 discrete difficulty levels and an engaging scoring system, Bit Op! introduces the user to binary encoding and bit manipulation.   Unlike the game it was inspired by, Bit Op! Provides both auditory and visual cues issued through a buzzer and an LED-strip respectively.  

The game consists of two user modes: Freeplay and Gameplay. In Freeplay, users can freely trigger the various inputs to familiarise themselves with the audio and visual cues associated with Push, Twist, and Pull. In Gameplay mode, players will complete 3 different levels of varying difficulty and scoring system and aim to maximise their final score.  

Each level of Gameplay mode consists of 8 rounds. At the start of each round, an action cue will be generated. When the player hears the sound or sees the respective colour, they must press the corresponding input while the sound and colour are still displayed. Their score will change according to whether the input provided was correct. The duration of each round in a level is twice as fast as the previous level. The player is given 1s to respond in the first level, 0.5s in the second and 0.25s in the third level. As the level changes, the scoring mode changes as well. An illustration on the scoring system can be found below.  

Between rounds, the progressive score is displayed on the LED strip located along the side of the Bit Op, lit in green if the player won the previous round, and red if they lost.  

### `bit_op` Bit Op! Instruction Manual
<img src="https://github.com/shaunnope/comp_struct_1d/blob/master/images/bitop_instruction_pg1.jpg" width="200">
<img src="https://github.com/shaunnope/comp_struct_1d/blob/master/images/bitop_instruction_pg2.jpg" width="200">

### `bit_op` Bit Op! Datapath
<img src="https://github.com/shaunnope/comp_struct_1d/blob/master/images/bitop_datapath.png" width="200">


### `bit_op` Bit Op! File Description
`au_top.luc` contains the top level functions that deal with physical IO.  
`alu.luc` ties together the 16 bit adder, multiplier, compare, boolean and shifter modules.  
`bop_alu_wdsel.luc` contains the ALU and selector muxes  
`bop_controlunit.luc` generates the control signals to support different states of the FSM.  
`bop_regfile.luc` defines the Register File that reads/writes data during gameplay.  
`bop_slwclk_rng.luc` contains the slow clock and RNG modules that generate a slower clock signal and random action signals during gameplay.   
`seven_seg.luc` controls the seven segment display on the IO Shield (not visible in final product, used for debugging).  
File names starting with `sixteen_bit` control the boolean, compare, adder, shifter and multiplier functions of the ALU.  

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
