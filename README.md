# Simplified Linux Shell

A lightweight command-line shell implemented in C for **COMP3511: Operating Systems** at The Hong Kong University of Science and Technology (HKUST).

The project explores Linux process management, POSIX system calls, inter-process communication, and file descriptor manipulation by implementing core shell functionality.

## Features

- **Command Execution:** Executes external programs using process creation and program execution system calls.
- **Built-in Commands:** Supports `cd` and `exit`.
- **Pipelines:** Connects multiple commands using pipes, supporting multi-stage pipelines.
- **Input Redirection:** Redirects standard input from a file using `<`.
- **Output Redirection:** Redirects standard output to a file using `>`.
- **Signal Handling:** Handles Ctrl+C (`SIGINT`) according to the assignment's requirements.
- **Command Parsing:** Processes commands with arguments separated by spaces or tabs.

## Technical Details

| Component | Description |
|---|---|
| Language | C |
| Environment | Linux |
| System interface | POSIX system calls |
| Process management | Process creation and execution |
| Inter-process communication | Pipes and file descriptors |
| I/O management | Input/output redirection |
| Build tools | GCC |

### Concepts Demonstrated

- Process creation and execution
- Parent and child process responsibilities
- File descriptor duplication and management
- Inter-process communication through pipes
- Standard input and output redirection
- Signal handling
- Command parsing and argument management
- Resource cleanup and error handling

## Build

Compile the shell using GCC:

```bash
gcc -pedantic -Wall -Wextra -std=c99 -o myshell myshell.c
```

## Run

Start the shell with:

```bash
./myshell
```

Enter commands at the shell prompt, for example:

```bash
ls
cat input.txt
cat input.txt | wc -l
cat < input.txt
echo "Hello, world!" > output.txt
cd ..
exit
```

The shell supports pipelines involving multiple commands, subject to the assignment's input constraints.

## Implementation Constraints

The implementation follows the assignment's restrictions:

- Written in C.
- Uses POSIX interfaces rather than `system()` or `popen()`.
- Supports command lines up to 256 characters.
- Supports up to 8 commands in a pipeline.
- Supports up to 8 arguments per command, excluding the terminating `NULL` pointer.
- Handles input and output redirection in either order.
- Does not combine pipelines and redirection, as specified by the assignment.

## Learning Outcomes

This project provided practical experience with Linux system programming and operating system concepts, particularly process execution, inter-process communication, file descriptors, signal handling, and shell behavior.

## Academic Context

**Course:** COMP3511 — Operating Systems  
**Institution:** The Hong Kong University of Science and Technology (HKUST)  
**Project:** Programming Assignment 1 — Simplified Linux Shell

This project was completed as coursework to practise operating systems and systems programming concepts.