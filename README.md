# Shell Implementation
### Salvador Jimenez Gomez  CS450

This project is a custom shell implementation written in C. It supports basic shell functionalities such as executing commands, redirections, pipes, running commands in the background, and handling lists of commands.

## Features

- **Command Execution**: Execute basic Unix commands.
- **Redirections**: Support for input (`<`) and output (`>`, `>>`) redirections.
- **Pipes**: Pipe (`|`) operator to chain commands.
- **Background Execution**: Support for running commands in the background using `&`.
- **Command Lists**: Ability to execute a list of commands separated by `;`.

## How It Works

The shell works by parsing the input command line into a structured representation that captures the command(s), along with any redirections, pipes, or background execution requests. It then executes these commands according to the parsed structure.

### Command Types

- `EXEC`: Represents a basic command execution.
- `REDIR`: Handles redirection of input/output.
- `PIPE`: Manages piping output from one command to the input of another.
- `LIST`: Executes a list of commands sequentially.
- `BACK`: Runs a command in the background.

### Parsing and Execution

The shell parses the input command line to identify the command type and its components, such as the command to execute, files for redirection, and commands to pipe. Based on the parsed command type, it then executes the appropriate action, such as running a process, setting up pipes, or handling file redirections.

## Compilation

To compile the shell, use the following command:

make clean
make
make qemu

NOTE: this assumes that you have qemu and xv6_riscv installed as well as homebrew. 

Here are the links to the shell implementation used for this lab

https://pdos.csail.mit.edu/6.828/2023/xv6.html



