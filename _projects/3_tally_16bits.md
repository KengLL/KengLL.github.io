---
layout: post
title: "TALLY: 16 bits float operation hardware"
image: "/img/in-project/tally_16bit.png"
tech:
  - name: "System Verilog"
    icon: "/img/tech/system_verilog.png"
description: TALLY is an accumulator-based architecture designed for simplicity and efficiency, utilizing a single accumulator register for basic arithmetic and data movement.
tags:
  - "Software Development"
---

# TALLY: An Accumulator-Based Architecture

## Overview
TALLY is an accumulator-based architecture designed for simplicity and efficiency in handling basic arithmetic and data movement. By relying on a single accumulator register, TALLY minimizes complexity and hardware needs, making it ideal for straightforward operations. The machine separates "move" and "add" instructions, ensuring a clear data flow and preventing redundant operations.

---

## Architectural Overview
TALLY does not require two read addresses for its register file, as it uses an accumulator with 4 opcode bits and 5 register address bits. The machine includes 32 registers, with the first register acting as the accumulator and the second register dedicated to storing overflow. The remaining registers serve as general-purpose storage for intermediate values or computations.

### Internal Operands
- **Registers**: 32 total registers. The first register is the accumulator, the second is for overflow, and the remaining 30 are general-purpose registers.
- **Accumulator**: By using the accumulator, TALLY simplifies instructions, eliminating the need to specify both registers when performing operations. This gives the system a lot of flexibility in executing operations.

### Control Flow (Branches)
- **Branching**: The architecture supports `beq` (branch if equal), `bne` (branch if not equal), and `jmp` (unconditional jump).
- **Target Addressing**: A lookup table stores target addresses, simplifying jump operations and enabling quick access to frequently used locations.
- **Branch Distance and Large Jumps**: With the lookup table, there are no inherent limits on branch distance. The table can handle any jump distance within the addressable memory.

### Addressing Modes
- **Direct Addressing (via Lookup Table for Instructions)**: The `jmp`, `beq`, and `bne` instructions use a lookup table for instruction memory, allowing efficient access to subroutines.
- **Indirect Addressing for Data Memory Access**: A pointer in a register is used to load a memory address, allowing indirect access to data.

---

## Programmer's Model [Lite]

### 4.1 Programming Strategy
To optimize performance, the programmer should prioritize loading essential values into registers at the start of the program, reducing the need for frequent memory access. The accumulator register (R0) should be used for intermediate calculations, and the overflow register (R1) should manage overflow during calculations. By using the lookup table for control flow, jumps and branches are straightforward, improving the efficiency of program execution.

### 4.2 ISA Compatibility
TALLY’s instruction set is not directly compatible with ISAs like MIPS or ARM due to the simplified design and the 9-bit instruction width. MIPS and ARM typically use 32-bit instructions and complex addressing modes, which do not fit within TALLY’s constraints. Instead, TALLY uses a more compact set of instructions and a lookup table for control flow, reducing complexity while meeting the specific needs of the programs.

---

## Individual Component Specification

### Top Level
- **Module File Name**: `top_level.sv`
- **Functionality Description**:
  - 32 registers and 32 direct memory addresses.
  - 16 operations, with 4 bits for opcode and 5 bits for register/immediate values.
  - The Program Counter (PC) advances each cycle, fetching the next instruction and handling branching.
  - The control unit distinguishes ALU operations from general operations based on the opcode and instruction bits, passing them to the ALU or adjusting control signals as needed for operations like load, store, and branching.

The TALLY architecture also includes a custom Verilog module for implementing 16-bit floating point operations, as well as separate machine code files and lookup tables for each program. These can be compiled using `compile_asm.py`, and the binary files are loaded into the system by uncommenting the appropriate lines in `PC_LUT.sv` and `instr_ROM.sv`.

---

## Conclusion
TALLY is a simplified yet efficient accumulator-based architecture, designed for basic arithmetic and data movement operations. The use of an accumulator register streamlines operations, reducing hardware complexity and enhancing flexibility in programming. With its efficient memory access and control flow handling via lookup tables, TALLY provides a powerful yet simple architecture for a variety of tasks.

---

**Acknowledgments**
Special thanks to the team for their efforts in designing and developing TALLY, and to the contributors who assisted in implementing the custom Verilog module and lookup tables.
