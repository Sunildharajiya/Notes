# Chapter 1: Introduction to Program Execution

## 1.1 Source Code and Machine Code
A computer cannot directly understand programming languages such as C, C++, Java, or Python. These languages are called high-level programming languages because they are designed to be readable and writable by humans.

When a programmer writes:
```c
int a = 5;
```
the computer does not understand the words int, a, or 5. To the CPU, this is merely a sequence of characters stored inside a text file.
The processor executes only machine instructions, which are binary patterns defined by its Instruction Set Architecture (ISA).
Therefore, before execution, every C program must be translated into machine code by a compiler.

#### Key Concepts
- `Source Code`: Human-readable program written in a programming language.
- `Machine Code`: Binary instructions that the CPU can execute directly.
- `Compiler`: Software that translates source code into machine code.


## 1.2 Program Storage
Before execution, every program exists as a file on secondary storage, such as an SSD or HDD.
For example:
```
Storage (SSD)

hello.c
hello.exe
photo.jpg
movie.mp4
```
These files are stored permanently because SSDs are non-volatile storage devices, meaning they retain information even when electrical power is removed.
A source file (.c) and an executable file are both simply files stored on secondary storage until the operating system loads them.

## 1.3 Role of Main Memory (RAM)
When the user executes a program, the operating system loads the executable into Random Access Memory (RAM).
RAM is a volatile semiconductor memory whose primary purpose is to provide the CPU with fast access to instructions and data currently required for execution.
Unlike SSDs, RAM loses its stored information when electrical power is removed.

#### Characteristics of RAM
- Volatile memory
- High-speed access
- Temporary storage
- Directly accessible by the CPU

## 1.4 Why Is It Called "Random Access Memory"?

The word Random does not mean "unpredictable."
Instead, it means that every memory location can be accessed directly in approximately the same amount of time, regardless of its position.
For example, reading data stored at memory address:
`0x00001000`
takes approximately the same time as reading:
`0xABCD1234`
This property distinguishes RAM from storage technologies that require sequential access.

## 1.5 Program Execution
After loading the executable into RAM, the operating system transfers control to the processor.
The CPU repeatedly performs the following cycle:
- Fetch an instruction from memory.
- Decode the instruction.
- Execute the instruction.
- Update the Program Counter (PC) to locate the next instruction.
This process is known as the Fetch–Decode–Execute Cycle, which forms the foundation of all modern processors.

## 1.6 Variables and Memory
Consider the following statement:
```
int a = 5;
```
The compiler allocates storage for the variable a.
During execution, the operating system reserves memory for the process, and the value 5 is stored at a specific memory address.
Conceptually:

| Address | Stored Value |
| -- | -- |
| 0x1000 | 5 |

The identifier a exists only in the source code and compiler's symbol information. The CPU manipulates memory addresses and values, not variable names.

## 1.7 Updating Variables
When the program executes:
`a = 20;`
the memory address associated with a remains unchanged.
Only the value stored at that address is modified.
Before:

| Address | Value |
| -- | -- |
| 0x1000 | 5| 

After:

| Address | Value |
| -- | -- |
| 0x1000 | 20 |

This operation is known as overwriting the previous value.

## 1.8 Data Representation in Memory
Main memory stores information only as binary bits (0 and 1).
For example:
`01000001`
By itself, this sequence has no inherent meaning.
Depending on the context established by the program and compiler, the same bits may represent:
- an integer,
- a character,
- a machine instruction,
- or part of another data structure.
Thus, memory stores bits, while software determines their interpretation.

### Engineering Summary
At the end of this chapter, you should understand the following principles:
- A.C source file is a human-readable text file.
- The CPU executes only machine instructions.
- The compiler translates source code into executable machine code.
- Executable files reside on secondary storage until loaded by the operating system.
- RAM temporarily stores executing programs and their data.
- Variables occupy memory locations identified by addresses.
- Memory stores binary information without intrinsic meaning; interpretation depends on the executing program.