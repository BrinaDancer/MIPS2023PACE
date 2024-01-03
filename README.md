5 stage Pipeline design for a 32-bit MIPS

The goal of this project is to better understand the fundamentals of pipelining and the MIPS
pipeline's implementation.

Description
5 stage Pipeline design for a 32-bit MIPS. The code is simulated using the EDAplayground
platform.

Objective
The CPU supports the following fundamental assembly instructions: LDUR, STUR, ADD, SUB,
ORR, AND, CBZ, B, and NOP. LDUR and STUR support instantaneous values when executing
specific operations to the registers module.
The processor is pipelined, enabling the execution of many instructions at once. Between each
stage of the processor's operation, buffers and caches are added to make this possible. Each
instruction takes less time to execute thanks to this optimization, which also guards against atomic
reads that happen in between register-base instructions. The hazard detection unit and the
forwarding unit are two extra modules in this implementation. Hazards are potential issues with a
processor's instruction pipeline. These risks may cause errors in the computation's output. The
processor implements a danger detecting unit and a forwarding unit to deal with loading hazards.
The pipeline is stopped by the hazard detecting unit, which also inserts a bubble (NOPS) until the
following instruction is read. When an instruction that requires the use of the loaded register is
immediately followed by an LDUR instruction, the hazard detecting unit is frequently employed.
The group also put into place a forwarding unit that, when an instruction in the EX stage requires
a computed value from a previous instruction, sends that computed value from the MEM or WB
stage of the pipeline to the EX stage. The most recent computed value can be used because
multiplexers in the EX stage pass values from the MEM and WB stages.

Simulation
To run this project, you will need to have an account on EDAplayground. Once you have an
account, you can follow these steps:
1. Log in to EDAplayground.
2. Click on the "New" button in the top left corner of the screen.
3. Choose "Verilog" as the language and give your project a name.
4. Copy the contents of the "design.v" file into the editor window.
5. Copy the contents of the "testbench.v" file into the editor window.
6. In tools and simulations choose “Icarus Verilog 0.9.7” to run
7. Check “Open EPWave” after run to see simulation waveforms.
8. Click the "Run" button to simulate the design.

Contributors
1. Sabrina Davidson
2. Bhavin Goswami
3. Harshal Patil
4. Harsh Patel
5. Damin Shah
