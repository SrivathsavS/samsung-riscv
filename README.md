# Samsung-RISCV
Samsung riscv program repo

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <div class="container">
        <h1>S Srivathsav</h1>
        <p><strong>College:</strong> New Horizon College of Engineering</p>
        <p><strong>Email ID:</strong> <a href="mailto:s.srivathsav04@gmail.com">s.srivathsav04@gmail.com</a></p>
        <p><strong>GitHub Profile:</strong> <a href="https://github.com/SrivathsavS" target="_blank">SrivathsavS</a></p>
        <p><strong>LinkedIn Profile:</strong> <a href="https://www.linkedin.com/in/s-srivathsav-42616a21a" target="_blank">S Srivathsav on LinkedIn</a></p>
        <h1><ins>TASK 1</ins><h/1>
        <h3>Step 1: Setting Up Ubuntu within VMBox</h3>
        

1. Install Ubuntu on VMBox.
2. Launch Ubuntu's terminal.

![Screenshot from 2025-01-06 10-40-12](https://github.com/user-attachments/assets/45244398-5f84-4ec6-9437-107e2992124d)
<h3>Step 2: Install Leafpad</h3> 

Run the following command to install Leafpad:
```bash
$ sudo apt install leafpad
```

<h3>Step 3: Compile and Run the C Code</h3>h3>

Compile the C code:
```
$ gcc filename.c
```

Run the compiled program:
```
$ ./a.out
```
<h3>Step 4: Compile C Code with RISC-V Compiler</h3>

Compile the C code using the RISC-V compiler:
```
$ riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o filename.o filename.c
```
List the compiled object file:
```
$ ls -ltr filename.o
```
<h3>Step 5: Display Assembly Code</h3>

Display the optimized assembly code for the main function:
```
$ riscv64-unknown-elf-objdump -d filename.o | less
```
Here is the output for the sum for numbers from 1 to n lab using c as well as risc-v compilation :

C compilation :

![Screenshot from 2025-01-06 08-55-14](https://github.com/user-attachments/assets/3a7b7dec-4f3e-44d3-86c0-aca596476ea1)

RISC-V :

![Screenshot from 2025-01-06 10-52-19](https://github.com/user-attachments/assets/efcd320a-7c24-40ae-8f4f-fc3ade96c0c7)



![Screenshot from 2025-01-06 10-17-17 (copy)](https://github.com/user-attachments/assets/1c168ce0-5c2e-47f2-9d13-d1ffbca9f96d)



![Screenshot from 2025-01-06 10-16-06](https://github.com/user-attachments/assets/aaeb626c-ab14-4feb-86c4-d2058e4fd653)




![Screenshot from 2025-01-06 10-20-38](https://github.com/user-attachments/assets/d282308a-2e10-4a8f-938c-6a591b379a47)



<h1><ins>TASK 2</ins></h1>

<h2>Write a simple c program :</h2>
<h3>C program to calculate area of a circle</h3>



![C_program](https://github.com/user-attachments/assets/0eab6427-aa44-4487-9d2d-4c11e178ad2e)

<h2>Compilation using Spike :</h2>
<h3>O1-</h3>

![Screenshot from 2025-01-13 22-28-19](https://github.com/user-attachments/assets/bc0543d2-31ba-4945-a2de-293e1026e0e8)

<h3>object dump for O1 -</h3>


![o1objdump](https://github.com/user-attachments/assets/27b338d4-a331-439f-a3ec-8ca6b8a2f123)

<h3>Ofast -</h3>

![Screenshot from 2025-01-13 22-23-00](https://github.com/user-attachments/assets/a7b45986-028d-4570-aaa0-ac8397133fc3)


<h3>Object dump for Ofast -</h3>

![ofastobjdump](https://github.com/user-attachments/assets/e145d3c3-599f-49b0-aafb-b3d46b0b62b1)


<h1><ins>TASK 3</ins></h1>
<h2>RISC-V Instructions</h2>

<h2>RISC-V uses six basic instruction formats:</h2></p>
<p><h3><u>1. <ins>R-Type:</ins></u></h3> For register-register operations (e.g., add, sub).</p>
<p><h3><u>2. <ins>I-Type:</ins></u></h3> For immediate operations and loads (e.g., addi, ld).</p>
<p><h3><u>3. <ins>S-Type:</ins></u></h3> For store instructions (e.g., sd).</p>
<p><h3><u>4. <ins>B-Type:</ins></u></h3> For branch instructions (e.g., beq, bne).</p>
<p><h3><u>5. <ins>U-Type:</ins></u></h3> For instructions like lui and auipc.</p>
<p><h3><u>6. <ins>J-Type:</ins></u></h3> For jump instructions (e.g., jal).</p>

<h2>Each format has fixed fields:</h2>

<p><h3>1. <ins>opcode:</ins></h3> Identifies the instruction type.</p>
<p><h3>2. <ins>funct3 and funct7</ins>:</h3> Further specify the instruction.</p>
<p><h3>3. <ins>rd, rs1, rs2</ins>:</h3> Register destinations and sources.</p>
<p><h3>4. <ins>imm:</ins>/h3> Immediate values (encoded differently depending on the format).</p>

<h2>Each instruction's binary code is derived by filling in the fields based on the instruction's format. For example:</h2>

    ld a2, 1800(gp):
        Type: I-Type
        Fields:
            opcode[6:0]: 0000011 (Load instruction).
            rd[11:7]: 01010 (a2).
            funct3[14:12]: 011 (Load double-word).
            rs1[19:15]: 00100 (gp).
            imm[31:20]: 011100000000 (1800 in decimal).
        Final binary: 01110000000000100011010110000011
        Hexadecimal: 0x7081b603
'''
<p>Then we need to identify the opcode, funct3, and funct7 values for each instruction.</p>
<p>Decode the immediate value formats for I-Type, S-Type, and J-Type instructions.</p>

<h2>RISC-V uses register aliases (x0 to x31), but their corresponding numbers are encoded in the instruction:</h2>

    x10 is a0 (binary: 01010).
    x11 is a1 (binary: 01011).
    x2 is sp (binary: 00010), and so on.

<h2>The objdump file : </h2>

![ofastobjdump](https://github.com/user-attachments/assets/679d6c42-d7d2-4d02-924c-4e30c569544d)

<h2> This has the following RISC-V instructions - </h2>
<p>1. ld</p>
<p>2. lui</p>
<p>3. addi</p>
<p>4. sd</p>
<p>5. jal</p>
<p>6. ret (pseudo-instruction for jalr x0, ra, 0)</p>
<p>7. auipc</p>
<p>8. beqz (pseudo-instruction for beq)</p>
<p>9. j (jump instruction)</p>
<p>10. sub</p>
<p>11. li (pseudo-instruction for addi x, x0, imm)</p>
<p>12. lw</p>
<p>13. jalr</p>
<p>14. bne</p>
<p>15. call (pseudo-instruction for jal)</p>

<h2> The 32-bit pattern for the above instructions are :</h2>

| #  | Instruction   |         32-bit pattern           | Opcode   | Funct3  | Funct7   | Imm/Offset           |
|----| ------------- | -------------------------------- | -------- | ------- | -------- | -------------------- |
| 1  | ld            | 01110000000000100011010110000011 | 0000011  | 011     | -        | 1800                 |
| 2  | lui           | 00000000001000010100110101101111 | 0110111  | -       | -        | 0x21000              |
| 3  | addi          | 11111111111100010000100100010011 | 0010011  | 000     | -        | -1 (Immediate)       |
| 4  | sd            | 00000000000101000011010010010011 | 0100011  | 011     | -        | Offset from rs1      |
| 5  | jal           | 00110100000000000000000011101111 | 1101111  | -       | -        | Offset to label      |
| 6  | ret           | 00000000000000000000000001100111 | 1100111  | 000     | -        | (Uses ra)            |
| 7  | auipc         | 11111111111100000110101000101111 | 0010111  | -       | -        | Upper Immediate      |
| 8  | beqz          | 00000000110100000110010011100011 | 1100011  | 000     | -        | Relative Offset      |
| 9  | j             | 00001100000000000000000011001111 | 1101111  | -       | -        | Offset to jump       |
| 10 | sub           | 01000000101001010000010110110011 | 0110011  | 000     | 0100000  | (From rs1 and rs2)   |
| 11 | li            | 11111111111100000000100010010011 | 0010011  | 000     | -        | -1 (Immediate)       |
| 12 | lw            | 00000000000101001000010010000011 | 0000011  | 010     | -        | Load address offset  |
| 13 | jalr          | 00000000000001000000000011100111 | 1100111  | 000     | -        | Indirect jump offset |
| 14 | bne           | 00000000000100000001010011100011 | 1100011  | 001     | -        | Relative Offset      |
| 15 | call          | 00000000000000000000000011101111 | 1101111  | -       | -        | Offset to function   |

<h1><ins>TASK 4</ins></h1>
<h2>RISC-V Simulation</h2>


This project provides a functional simulation of a custom RISC-V core (iiitb_rv32i) using Verilog. The design includes a testbench for validation, generates waveforms for debugging, and demonstrates the execution of a simple instruction set.
<p><h2><ins>Features:</h2></ins>

   <p><ins></ins>RISC-V Core Implementation:</ins> Includes a Verilog netlist for a 32-bit RISC-V core.</p> 
   <p><ins></ins>Instruction Set Support:</ins> Supports basic arithmetic, logical, memory, and branch instructions.</p> 
   <p><ins></ins>Testbench Validation:</ins> Simulates the core's functionality with an automated testbench.</p> 
   <p><ins></ins>Waveform Analysis:</ins> Captures and visualizes waveforms using GTKWave.</p> 

<p><h2><ins>Simulation Steps:</ins></h2>

<h3>1. Compile the Design:</h3>
```
iverilog -o riscv_sim.out iiitb_rv32i_tb.v iiitb_rv32i.v
```
<h3>2. Run the Simulation:</h3>
```
vvp riscv_sim.out
```
![Screenshot from 2025-01-23 21-52-49](https://github.com/user-attachments/assets/62b468d9-e413-4bd9-bad0-5f381db97284)


<h3>3. View the Waveforms:</h3>
```
gtkwave iiitb_rv32i.vcd

```
![Screenshot from 2025-01-23 21-51-34](https://github.com/user-attachments/assets/88b3d5cf-0d07-4070-8bc5-834ea19d3498)
[task4.pdf](https://github.com/user-attachments/files/18523803/task4.pdf)
