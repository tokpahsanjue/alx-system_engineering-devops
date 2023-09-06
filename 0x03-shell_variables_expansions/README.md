# Shell Basics README
This README provides an overview of essential shell basics and commands. It covers a range of topics, from shell initialization to executing commands from a file in the current shell.

## What happens when you type `$ ls -l *.txt`

When you type `$ ls -l *.txt` in the shell, you are instructing the system to list all files in the current directory that have a `.txt` extension, displaying them in a long format (`-l`) that includes detailed information such as file permissions, ownership, size, and modification date.

## Shell Initialization Files

### /etc/profile and /etc/profile.d

- `/etc/profile`: This file is a system-wide initialization script executed when a user logs in. It sets environment variables and configurations that apply to all users.

- `/etc/profile.d`: This directory contains additional shell initialization scripts that are sourced by `/etc/profile`. It allows for modular configuration, making it easier to manage system-wide settings.

### ~/.bashrc

- `~/.bashrc`: This file is a user-specific initialization script for the Bash shell. It is executed when a user opens a new interactive shell session. Users can customize their environment variables and aliases in this file.

## Variables

### Local vs. Global Variables

- **Local variables**: These are variables defined within a specific shell session or script and have limited scope, typically available only in that specific context.

- **Global variables**: These are variables that persist across shell sessions and are available to all commands and scripts run by the user. They are typically set in shell initialization files.

### Reserved Variables

- A **reserved variable** is a special variable with a predefined meaning in the shell. Examples include `HOME`, `PATH`, and `PS1`.

### Creating, Updating, and Deleting Shell Variables

- To create or update a shell variable, you can use the `variable_name=value` syntax, e.g., `my_var="Hello"`.

- To delete a shell variable, use the `unset` command, e.g., `unset my_var`.

### Roles of Reserved Variables

- **HOME**: Specifies the user's home directory.
- **PATH**: Defines the directories where the shell looks for executable commands.
- **PS1**: Sets the shell prompt format.

## Special Parameters

- **Special parameters** are built-in variables with specific meanings. They are used to access information about the shell environment and command execution.

## Special Parameter `$?`

- `$?` is a special parameter that holds the exit status of the last executed command. A value of `0` typically indicates success, while non-zero values indicate errors.

## Expansions

- **Expansions** are mechanisms for manipulating and substituting values in shell commands and scripts.

### Single vs. Double Quotes

- Single quotes (`'`) preserve the literal value of all characters within them. Variables and special characters are not expanded.

- Double quotes (`"`) allow variable and command substitution. Variables and special characters within double quotes are expanded.

### Command Substitution

- Command substitution allows you to execute a command within a command and capture its output. You can use `$()` or backticks (`` ` ``) for command substitution.

## Shell Arithmetic

- Shell provides basic arithmetic operations using expressions like `((expression))` or `let`. For example, `result=$((2 + 3))` or `let "result=2+3"` will store the value `5` in the variable `result`.

## The `alias` Command

- You can create aliases using the `alias` command to define shortcuts for longer commands. For example, `alias ll='ls -l'` creates an alias to list files in long format.

- To list all aliases, use the `alias` command without arguments.

- To temporarily disable an alias, prepend a backslash to the alias name, e.g., `\ll` will temporarily disable the `ll` alias.

## Executing Commands from a File

- To execute commands from a file in the current shell, use the `source` or `.` command followed by the file's path, e.g., `source my_script.sh` or `. my_script.sh`.

This README provides an introduction to fundamental shell concepts and commands. For more detailed information, consult the respective man pages and online documentation for your specific shell (e.g., `bash`, `sh`, `zsh`, etc.).
