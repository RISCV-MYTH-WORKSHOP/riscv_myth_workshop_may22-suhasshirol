**<br />OSFPGA RISC-V Workshop**
<br />
<br />The following repository contains all the information that's needed to a build a 4-stage Pipelined RISC-V Core which is designed during the RISC-V MYTH Workshop. The core supports the RV32I Base Integer Instruction Set. It is developed and implemented in TL-Verilog on Makerchip platform.
<br />![risc-v_banner](https://user-images.githubusercontent.com/66528639/171032757-e54681bb-c60f-4a86-b0d0-a28441a54018.png)

**<br />Content of Workshop**
**<br />Day 1 : Introduction to RISC-V ISA and GNU compiler toolchain

<br />Part 1: Introduction to RISC-V basic keywords
<br />Part 2: Labwork for RISC-V software toolchain
<br />Part 3: Integer number representation
<br />
<br />Day 2: Introduction to ABI and basic verification flow
<br />Part 1: Application Binary interface (ABI)
<br />Part 2: Lab work using ABI function calls
<br />Part 3: Basic verification flow using iverilog
<br />
<br />Day 3 : Digital Logic with TL-Verilog and Makerchip
<br />Part 1: Combinational logic in TL-Verilog using Makerchip
<br />Part 2: Sequential and pipelined logic
<br />Part 3: Validity
<br />Part 4: Hierarchy
<br />
<br />Day 4 : Basic RISC-V CPU micro-architecture
<br />Part 1: Microarchitecture and testbench for a simple RISC-V CPU
<br />Part 2: Fetch, decode, and execute logic
<br />Part 3: RISC-V control logic
<br />
<br />Day 5 : Complete Pipelined RISC-V CPU micro-architecture/store
<br />Part 1: Pipelining the CPU
<br />Part 2: Load and store instructions and memory
<br />Part 3: Completing the RISC-V CPU**
<br />
<br />**Day 1**
<br />Introduction to RISC-V ISA and GNU compiler toolchain

<br />**1. Introduction to RISC-V basic keywords**
<br />![1](https://user-images.githubusercontent.com/66528639/170438295-96af3bc3-55a1-4f7b-b473-2ce3fbf7c3d0.jpg)
<br />
<br />![2](https://user-images.githubusercontent.com/66528639/170438416-7b6a3424-0de7-413a-8b01-591a59aaa0b6.jpg)
<br />
<br />![3](https://user-images.githubusercontent.com/66528639/170438500-1e7dbad3-1ac3-46dc-80e2-636be594ad94.jpg)
<br />
<br />![4](https://user-images.githubusercontent.com/66528639/170438544-119bd6f4-9a3f-48a3-a08d-92f31fa23040.jpg)
<br />
<br />![7](https://user-images.githubusercontent.com/66528639/170438772-3f784bc8-d685-4691-a2d1-21220521a2a9.jpg)
<br />
<br />Pseudo Instructions
<br />
<br />![8](https://user-images.githubusercontent.com/66528639/170438919-a7693724-5dc3-43b0-8665-453052dcaa2e.jpg)
<br />
<br />Base Integer Instructions
<br />
<br />![9](https://user-images.githubusercontent.com/66528639/170439012-d6e3a867-f7a5-4bd4-ae28-a7982de60c50.jpg)
<br />
<br />Multiply Extension RV64M Instructions
<br />
<br />![10](https://user-images.githubusercontent.com/66528639/170439188-bf4792e9-ce55-4489-a08e-081c1c9acafd.jpg)
<br />
<br />Single and Double Floating Point Instructions (RV64F and RV64D)
<br />
<br />![11](https://user-images.githubusercontent.com/66528639/170439385-78e9a10c-9416-4db1-8991-d0eca851c05d.jpg)
<br />
<br />Application Binary Interface Instructions
<br />
<br />![12](https://user-images.githubusercontent.com/66528639/170439483-e60fe255-1148-4241-8c8f-29b53587d6ae.jpg)
<br />
<br />Memory Allocation and Stack Pointer Instructions
<br />





<br />**Day 2**
<br />
**<br />1.Application Binary interface (ABI)**
<br />![1](https://user-images.githubusercontent.com/66528639/170626363-66fe065c-f95a-42e0-9b84-842684ad209e.jpg)
<br />
<br />Application Binary Interface
<br />![2_ABI](https://user-images.githubusercontent.com/66528639/170626388-46b16aa8-c56e-419d-a109-ef19c95c2575.jpg)
<br />
<br />Application Binary Interface overview
<br />
<br />![3_Memory](https://user-images.githubusercontent.com/66528639/170626415-b0f27766-15ab-4189-b141-b8e77ffbba0d.jpg)
<br />
<br />Application Binary Interface Registers
<br />
<br />![4_32bit_register](https://user-images.githubusercontent.com/66528639/170626600-4dbce797-97d6-4dd5-83a0-baf7326b7487.jpg)
<br />
<br />Application Binary Interface Registers Type
<br />
<br />![4_I_type_Instruction](https://user-images.githubusercontent.com/66528639/170626748-f829c2b7-f401-48a3-8679-291fc2268789.jpg)
<br />
<br />Application Binary Interface Registers Type-I
<br />
<br />![4_R_type_Instruction](https://user-images.githubusercontent.com/66528639/170626807-9fac6fe8-a37a-49a1-bcff-1dbb5895e2a8.jpg)
<br />
<br />Application Binary Interface Registers Type-R
<br />
<br />![4_S_type_Instruction](https://user-images.githubusercontent.com/66528639/170626874-41950665-f0b4-4c6a-b45a-1528c4407d06.jpg)
<br />
<br />Application Binary Interface Registers Type-S
<br />
<br />![5_Registers](https://user-images.githubusercontent.com/66528639/170626981-35586fe7-b5eb-4949-bd8e-7ca9b4a46a12.jpg)
<br />
<br />Application Binary Interface Registers register usage
<br />

**<br />2. Lab work using ABI function calls**
<br />
<br />![6_CtoASM_Program](https://user-images.githubusercontent.com/66528639/170627095-7f49ba4d-2c38-4576-ba7d-8998a2bf6c46.jpg)
<br />
<br />Flow diagram for C program using ASM language
<br />
<br />![7_lab_CtoASM_results](https://user-images.githubusercontent.com/66528639/170627210-dcb342bd-70d8-4af6-9f2d-036b4ec8b708.jpg)
<br />
<br />C program and ASM program with commands and results
<br />
<br />![8_lab_object_CtoASM_results](https://user-images.githubusercontent.com/66528639/170627300-1c0eab8e-beea-4d3f-bdcb-a3b16724f2ee.jpg)
<br />
<br />Object program C to ASM
<br />
<br />![9_CtoRISCV_Conversion](https://user-images.githubusercontent.com/66528639/170627436-235bfaf3-6b80-4a25-b655-c16a422d6110.jpg)
<br />
<br />C porgram on RISCV CPU

**<br />3. Basic verification flow using iverilog**
<br />
<br />![10_Program_to_convert_Hex](https://user-images.githubusercontent.com/66528639/170631345-080f1e80-f4da-497f-a122-22e691431fc7.jpg)
<br />Program to convert C program to Hex
<br />
<br />![10_results](https://user-images.githubusercontent.com/66528639/170631421-e65c89f6-70f6-44e6-87f3-f4193d2205c2.jpg)
<br />
<br />Results of program to find sum of N=2
<br />
<br />![10_Hex_data](https://user-images.githubusercontent.com/66528639/170631600-3aa00698-cf92-44ed-bb66-6c0e711b2d64.jpg)
<br />
<br />Hex converted file
