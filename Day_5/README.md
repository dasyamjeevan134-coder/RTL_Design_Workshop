# Day 5 - Case Statements, Incomplete Assignments and Logic Synthesis

Day 5 focuses on understanding different RTL coding styles and
their effect on synthesized hardware.

The experiments mainly deal with `case` statements, incomplete
conditional assignments, MUX and DEMUX generation, and a Ripple
Carry Adder (RCA).

The RTL designs were simulated to verify their functionality.
The designs were then synthesized using Yosys and the generated
netlists/block diagrams were studied to understand how different
coding styles are converted into hardware.

---

## Contents

1. [Objective](#1-objective)
2. [Bad Case](#2-bad-case)
3. [Complete Case](#3-complete-case)
4. [DEMUX using Case](#4-demux-using-case)
5. [DEMUX using Generate](#5-demux-using-generate)
6. [Incomplete If-Else](#6-incomplete-if-else)
7. [Incomplete Case](#7-incomplete-case)
8. [MUX using Generate](#8-mux-using-generate)
9. [Partial Case](#9-partial-case)
10. [Ripple Carry Adder](#10-ripple-carry-adder)
11. [Overall Learning](#11-overall-learning)
12. [Conclusion](#12-conclusion)

---

# 1. Objective

The main objectives of Day 5 are:

- To understand different RTL conditional coding styles.
- To study the working of `case` statements.
- To understand the effect of incomplete conditions.
- To observe how incomplete assignments can lead to unwanted
  hardware such as latches.
- To study MUX and DEMUX implementation using RTL constructs.
- To understand generate-based hardware structures.
- To compare RTL descriptions with synthesized netlists.
- To verify designs using simulation waveforms.
- To understand the implementation of a Ripple Carry Adder.

---

# 2. Bad Case

The bad case experiment demonstrates an improper or incomplete
use of a `case` statement.

When all possible input conditions are not properly assigned,
the synthesis tool may infer storage elements or produce
unexpected hardware behavior.

The design was simulated first and the waveform was examined.
The corresponding synthesized hardware was then observed.

### Files

- `bad_case waveform.png`
- `badcase gls.png`
- `badcase netlist and waveform.png`

### Waveform

The waveform was used to check the output for different input
conditions.

### Synthesis

The synthesized representation helps identify the hardware
generated from the incomplete case description.

---

# 3. Complete Case

A complete case statement provides assignments for all required
conditions.

This coding style helps describe combinational logic correctly
and avoids unnecessary storage elements.

The RTL was synthesized and the generated netlist and block
diagram were studied.

### Files

- `comp_case_netlist and blockdia...`

### Result

The experiment showed how a properly specified case statement
can produce the intended combinational hardware.

---

# 4. DEMUX using Case

A demultiplexer transfers one input signal to one of several
outputs according to the select signal.

In this experiment, a DEMUX was described using a case-based
RTL approach.

The design was simulated and the output response was checked
for different select combinations.

### File

- `demux_case_waveforms.png`

### Result

The waveform demonstrates that the input is routed to the
appropriate output depending on the select value.

---

# 5. DEMUX using Generate

In this experiment, a DEMUX was implemented using a generate
construct.

The generate statement is useful when a hardware structure
contains repeated logic.

Instead of writing every hardware connection individually,
generate constructs can create multiple similar structures.

### File

- `demux_generate_waveform.png`

### Result

The waveform was used to verify that the generated DEMUX
produces the expected output for different select inputs.

---

# 6. Incomplete If-Else

This experiment demonstrates the effect of an incomplete
`if-else` description in combinational RTL.

When an output is not assigned for every possible condition,
the synthesis tool may preserve the previous value of the
output.

This can result in latch inference.

### Files

- `incomp_if1 netlist and blockdia...`
- `incomp_if1_waveform.png`
- `incomp_if2 netlist and blockdia...`
- `incomp_if2 waveform.png`

### Result

The experiments show why combinational outputs should normally
be assigned for every possible input condition.

---

# 7. Incomplete Case

An incomplete case statement does not explicitly define the
output for every possible input combination.

This can cause the synthesis tool to infer storage behavior
depending on the RTL description.

### Files

- `incomp_case_netlist and blockdi...`
- `incompcasewaveform.png`

### Result

The simulation and synthesized representation were compared
to understand the effect of missing case assignments.

This experiment emphasizes the importance of writing complete
combinational RTL.

---

# 8. MUX using Generate

A multiplexer selects one input from multiple inputs based on
the select signal.

In this experiment, a MUX structure was created using the
generate construct.

Generate blocks are useful for describing repeated hardware
connections in a compact manner.

### Files

- `mux_generate_netlist and block...`
- `muxgenerate waveform.png`

### Result

The waveform verifies the MUX selection operation, while the
synthesized netlist shows the hardware structure created by
Yosys.

---

# 9. Partial Case

A partial case statement specifies only some of the possible
conditions.

If the remaining conditions are not assigned appropriately,
the synthesis tool may infer additional hardware.

This experiment was used to understand the difference between
a complete case description and a partial case description.

### File

- `partial_case_netlist and blockdia...`

### Result

The synthesized result demonstrates how the RTL coding style
affects the resulting hardware.

---

# 10. Ripple Carry Adder

The Ripple Carry Adder (RCA) is a digital arithmetic circuit
used to perform binary addition.

It is formed by connecting multiple full adders in sequence.
The carry output of one full adder becomes the carry input of
the next full adder.

The carry therefore propagates from the least significant bit
towards the most significant bit.

### File

- `rca waveform.png`

### Working

For each bit position:

- Two input bits are added.
- The incoming carry is included.
- A sum output is generated.
- The carry is passed to the next stage.

### Result

The waveform was used to verify the addition operation and
observe the propagation of the carry signal through the
different stages.

---

# 11. Overall Learning

From the Day 5 experiments, I learned:

- The syntax and behavior of case statements.
- The importance of complete assignments in combinational RTL.
- The difference between complete and incomplete case logic.
- How incomplete `if-else` statements can result in latch
  inference.
- How incomplete case statements can affect synthesized
  hardware.
- How a DEMUX can be described using a case statement.
- How generate constructs can be used to create repeated
  hardware.
- How a MUX can be implemented using generate-based logic.
- How RTL coding style influences synthesis results.
- How to analyze synthesized netlists and block diagrams.
- How to verify RTL functionality using waveforms.
- The basic structure and operation of a Ripple Carry Adder.
- The importance of writing synthesizable and complete RTL
  descriptions.

---

# 12. Conclusion

Day 5 provided practical understanding of RTL coding styles
and their impact on hardware synthesis.

The experiments with case statements and incomplete
conditional logic showed why every required condition should
be handled carefully in combinational designs.

MUX and DEMUX implementations demonstrated how different RTL
constructs such as `case` and `generate` can be used to describe
hardware.

The Ripple Carry Adder experiment further helped in
understanding the implementation of arithmetic circuits using
basic digital logic.

Overall, the session improved my understanding of RTL design,
simulation, synthesis, netlist analysis, and hardware
optimization.
