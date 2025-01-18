# VHDL Counter Overflow Bug
This repository demonstrates a common subtle bug in VHDL code: an integer counter that overflows due to a potential race condition or glitch in simulation. The `buggy_counter.vhdl` file contains the erroneous code. The `fixed_counter.vhdl` provides a corrected version that avoids this issue. 

## The Bug
The original counter uses a simple `if count = 15 then` check to reset the counter.  However, if there is a race condition or a simulation glitch, it is possible that the counter could increment past 15 before this condition is properly evaluated, causing incorrect behavior.

## The Solution
The solution involves using a more robust condition check or using a different approach altogether. The improved counter in `fixed_counter.vhdl` demonstrates a safer method for handling the counter reset to prevent the counter from skipping the reset condition.