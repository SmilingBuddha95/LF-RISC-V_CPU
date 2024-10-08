LF-RISC-V CPU Project - README
# LF-RISC-V CPU
This repository contains the full implementation of a RISC-V CPU core, developed as part of the Linux Foundation's course on designing RISC-V architecture. The project is divided into several stages, each addressing different aspects of CPU design, from conceptual block diagrams to functional tests of the instruction set.
## Project Overview
The core components of this CPU include:
- **Instruction Fetch (IF):** Fetches instructions from memory.
- **Instruction Decode (ID):** Decodes the instructions to identify operations. - **Execution Unit (EX):** Handles arithmetic and logical operations.
- **Memory Access (MEM):** Reads from and writes to memory.
- **Write Back (WB):** Writes results back to the register file.
All stages of the CPU pipeline are implemented in Verilog HDL. The control flow and state machines handle data hazards and stalls, ensuring correct instruction execution even in the presence of pipeline dependencies.
## Tests and Validation
Extensive testing has been performed to validate the correct behavior of the CPU. Tests include: - **Basic Arithmetic Operations:** Testing ADD, SUB, MUL, and DIV instructions.
- **Logical Operations:** Verifying AND, OR, XOR, and shift operations.
- **Branching and Jump Instructions:** Ensuring correct branching and conditional jumps.
- **Memory Instructions:** Load and store operations have been validated using a memory model for correctness.
The testing framework relies on a combination of Verilog testbenches and simulation tools such as ModelSim, with various test cases developed to cover both typical and edge cases. Each module is separately tested before integrating it into the pipeline.
## Installation
1. Clone this repository: ```bash
git clone https://github.com/SmilingBuddha95/LF-RISC-V_CPU.git cd LF-RISC-V_CPU
```
2. Ensure you have a compatible Verilog simulator like ModelSim or Icarus Verilog installed. 3. Run the simulation files in the `test/` folder to validate the design:
```bash
iverilog -o cpu_sim test/cpu_tb.v vvp cpu_sim
```
## File Structure
- `src/`: Contains the Verilog source code for the CPU core.
- `test/`: Contains the testbenches and validation scripts.
- `docs/`: Contains detailed documentation and block diagrams explaining the architecture.
## Future Work
Future enhancements planned for the CPU core include:
- Implementation of more complex instructions, including floating-point operations. - Optimization of the memory access stage to improve performance.
## License
This project is licensed under the MIT License.
