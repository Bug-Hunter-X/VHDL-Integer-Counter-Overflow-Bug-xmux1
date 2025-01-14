# VHDL Integer Counter Overflow Bug

This repository demonstrates a subtle bug in a VHDL counter implementation that can lead to unexpected behavior. The `buggy_counter.vhdl` file contains the buggy code. The counter uses an integer type with a specified range. An issue occurs when the counter reaches the maximum value in its range. The comparison and assignment within the process might not handle this edge case correctly.

The `fixed_counter.vhdl` file shows the corrected version, addressing the overflow problem.

## How to Reproduce

1. Synthesize and simulate `buggy_counter.vhdl`.
2. Observe the counter's behavior when it reaches the upper bound of its range.
3. Compare this to the behavior of the corrected code in `fixed_counter.vhdl`. 

## Solution

The core issue lies in the way the counter handles the maximum value (15).  The corrected code uses a more robust approach, providing cleaner, more reliable behavior.