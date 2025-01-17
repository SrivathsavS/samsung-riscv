# samsung-riscv
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
        <h1>TASK 1<h/1>
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



<h1>TASK 2</h1>

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


