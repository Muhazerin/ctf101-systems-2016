#ctf101 Systems 2016 Lesson Plan

## Assumptions

We assume that participants have the following pre-requisite knowledge:

1. Basic programming in any scripting language
2. Some elementary familiarity with C
3. The tools and ability to ssh into their provided shell accounts given out the 
previous day

## Topics to Cover

0. Approach
1. Overview of Systems Exploitation
2. Offensive Python 101
3. Input/Output 
4. Types of Compromise
5. Illustration of Compromise in Target Python Applications
6. Data Representation and Endianness
7. C and x86-64 Assembly
8. Memory Layout
9. Stack Frames
10. Calling Conventions
11. Memory Corruption Vulnerabilities
12. Other Vulnerabilities
13. Mitigations and Bypasses

## 0. Approach 

In this session, we shift our focus from web technologies to systems 
applications. These refer to applications that run 'natively' on your machines 
or on remote machines. For example, programs like calc.exe or /bin/ls fall under 
the category of systems applications. We will be learning how to delve deep into 
the inner workings of these programs, discovering vulnerabilities, and 
exploiting these vulnerabilities to achieve a compromise objective.

We will take an extremely incremental approach to the lesson where our approach 
to the vulnerability discovery and exploit writing process is applied to easy 
to understand vulnerable Python scripts before tackling compiled binaries that 
require the extra step of reverse engineering of x86-64 assembly and an 
understanding of memory layout. 

It is hoped that by the end of the workshop, participants will have the required 
knowledge of the tools and skills needed to further progress onto more advanced 
topics in the reverse engineering and exploitation of systems applications.

## 1. Overview of Systems Exploitation

Systems security is an extremely large domain. Basically, anything that runs on 
a system, local or remote, is considered a systems application. Typically, the 
primary target we look at in systems security are 'binaries'. These are compiled 
applications that run natively on the processor of the machine. These binaries 
could have been written in a variety of languages such as Golang or OCaml, but 
most are probably written in C or C++. The important point to note here is that 
obtaining an understanding of what the program does is not as simple as opening 
the file in a text editor and hoping for the source code to appear. The result 
is literally a 'binary' mess.

What is to be done then is to transform the raw native bytecode that make up the
binary into something understandable by a human. In this workshop, we will look
at turning the bytecode into x86-64 assembly in a process called disassembly.
The mapping between the raw bytecode and x86-64 instructions is sufficiently
close enough to understand what happens to the processor during program 
execution. We will go further in depth into assembly language later on. 

Vulnerabilities in these binaries come in two flavours: memory corruption and 
logic vulnerabilties. Memory corruption vulnerabilties typically stem from a bug
in the code that provides a vector for an attacker to corrupt regions of memory
in such a way that the new values cause unintended consequences during program
execution. Logic vulnerabilities cause unintended consequences directly as a
result of faulty programming logic.

Interpreted programs such as ruby scripts or compiled Java bytecode also fall
under our domain. However, they primarily only contain logic vulnerabilities
(there might be extremely esoteric counterexamples, though).

We will craft our exploit code in the python language. Hopefully most of you are
already familiar with it but we will begin with a short crash course on the
language and required features of it.

## 2. Offensive Python 101

- How to invoke python (cmd, interpreter, script)
- Language syntax
- Important module use

## 3. Input/Output

- Arguments
- Stdin/Stdout/Stderr
- Files
- Sockets

## 4. Types of Compromise

## 5. Illustration of Compromise in Target Python Applications

## 6. Data Representation and Endianness

## 7. C and x86-64 Assembly

## 8. Memory Layout

## 9. Stack Frames

## 10. Calling Conventions

## 11. Memory Corruption Vulnerabilities

## 12. Other Vulnerabilities

## 13. Mitigations and Bypasses

