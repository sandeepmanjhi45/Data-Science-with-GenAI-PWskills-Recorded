# How Computers and Programming Languages Work (Simple Notes)

## CPU (the brain of the computer)
The CPU is the part of the computer that does the thinking. It follows the instructions that programs give it.

It does three main jobs:
- Runs instructions
- Does calculations and makes decisions
- Manages the other parts of the computer

## Memory (where the computer keeps things)

### Primary memory (working memory)
This is the memory the computer uses while it is working.

| Type | What it does | Lost when power is off? | Speed |
|------|--------------|-------------------------|-------|
| **RAM** | Holds the apps and files you are using right now | Yes | Fast |
| **ROM** | Holds the basic start-up instructions (BIOS) | No | Slower |

**Example:** RAM is like your study desk. You keep only the books you are using right now on it. When you leave, the desk is cleared.

### Secondary memory (storage)
This is where your files stay for a long time, even when the computer is off.

| Type | Simple meaning | Used for |
|------|----------------|----------|
| **SSD** | Fast flash storage | Quick start-up and fast apps |
| **HDD** | Spinning disk, cheaper | Storing lots of files and backups |
| **USB flash drive** | Small and portable | Moving files between computers |

**Example:** Secondary memory is like your bookshelf. Books stay there until you remove them.

### Memory hierarchy
The closer memory is to the CPU, the faster it is, but the less it can hold.

CPU registers → Cache → Main memory (RAM) → Hard disk → Optical disk → Magnetic tape

Going down this list, memory gets slower but can store more.

## Programming languages

### High-level languages
Easy for humans to read and write. They look a bit like English.
- **Python:** easy to learn, used for web, AI and automation
- **Java:** used for company software and Android apps
- **C++:** can work at both high and low level
- **JavaScript:** runs in the browser, used for websites
- Others: Ruby, PHP, Swift

### Low-level languages
Very close to the computer's own language, giving more control over hardware.
- **Machine language:** only 0s and 1s. The CPU runs it directly, but it is very hard to write.
- **Assembly language:** short word-like commands such as MOV, ADD and SUB. It is easier than 0s and 1s, but needs an **assembler** to turn it into machine code.

## Interpreter and compiler
The computer only understands 0s and 1s, so our code must be translated first. There are two ways to do it.

| | Interpreter | Compiler |
|---|-------------|----------|
| How it works | Translates and runs **line by line** | Translates the **whole program first**, then runs it |
| Speed | Slower | Faster |
| Errors | Stops at the first error and shows it | Finds many errors before the program runs |
| Output | No separate file | Creates a ready-to-run file (like .exe) |
| Examples | Python, JavaScript, Ruby | C, C++, Rust, Go |

**Example:**
- An interpreter is like a live translator who translates each sentence as you speak.
- A compiler is like a translator who translates the whole book first and then gives it to you.

## Where Python fits
Python is a high-level, interpreted language. The main interpreter is **CPython**.

How Python code runs:
1. You write code in a `.py` file.
2. Python turns it into **bytecode**, a simpler in-between form (saved as `.pyc`).
3. The **Python Virtual Machine (PVM)** runs the bytecode.

So Python is a mix of both: it is compiled to bytecode and then interpreted.

## Remember
- CPU is the brain, RAM is the working desk, and storage is the bookshelf.
- High-level languages are easy for humans, and low-level languages are close to the machine.
- An interpreter works line by line, and a compiler works on the whole program.
- Python is high-level and interpreted.
