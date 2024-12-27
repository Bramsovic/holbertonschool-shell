# Project: Shell Initialization Files, Variables and Expansions

This project focuses on shell initialization files, environment variables, local variables, arithmetic operations, aliases, and expansions in **Bash**. Each **bash** script is exactly two lines long, with `#!/bin/bash` as the first line.

## Table of Contents
1. [Learning Objectives](#learning-objectives)  
2. [Requirements](#requirements)  
3. [Project Structure](#project-structure)  
4. [Script Descriptions](#script-descriptions)  
5. [Resources](#resources)

---

## Learning Objectives

By the end of this project, you should be able to explain, without Google or external help:

- **General**
  - What happens when you type `$ ls -l *.txt`
- **Shell Initialization Files**
  - The purpose of `/etc/profile`, `/etc/profile.d/` directory
  - The purpose of `~/.bashrc`
- **Variables**
  - Differences between local and global variables
  - What a reserved variable is
  - How to create, update, and delete shell variables
  - Roles of reserved variables like `HOME`, `PATH`, and `PS1`
  - What special parameters are, and what `$?` stands for
- **Expansions**
  - What expansions are and how to use them (e.g., command substitution)
  - Differences between single and double quotes
  - Command substitution with `$( )` and backticks
- **Shell Arithmetic**
  - How to do arithmetic operations in the shell
- **Alias Command**
  - Creating aliases, listing them, and disabling them
- **Other Topics**
  - Executing commands from a file in the current shell using `.` or `source`

---

## Requirements

1. **Allowed editors**: `vi`, `vim`, `emacs`.  
2. **Scripts tested on**: Ubuntu 20.04 LTS.  
3. **Each script must be exactly 2 lines** (`wc -l file` returns `2`).  
4. **All files must end with a newline**.  
5. **The first line of each script**: `#!/bin/bash`.  
6. A `README.md` at the root describing each script.  
7. **No** `&&`, `||`, or `;` in the scripts.  
8. **No** `bc`, `sed`, or `awk` allowed.  
9. All scripts must be **executable**: `chmod u+x filename`.

---

## Project Structure

```
init_files_variables_and_expansions
├── 0-alias
├── 1-hello_you
├── 2-path
├── 3-paths
├── 4-global_variables
├── 5-local_variables
├── 6-create_local_variable
├── 7-create_global_variable
├── 8-true_knowledge
├── 9-divide_and_rule
├── 10-love_exponent_breath
├── 11-binary_to_decimal
├── 12-combinations
├── 13-print_float
├── 14-decimal_to_hexadecimal
└── README.md
```

---

## Script Descriptions

> **Note**: Each script is exactly 2 lines, with the first line being `#!/bin/bash`.

1. **0-alias**  
   - Creates an alias named `ls` that runs `rm *`.

2. **1-hello_you**  
   - Prints `hello user` where `user` is the current Linux user.

3. **2-path**  
   - Adds `/action` to the `PATH` as the **last** directory searched when executing programs.

4. **3-paths**  
   - Counts the number of directories in the `PATH`.

5. **4-global_variables**  
   - Lists all **environment** variables (like using `printenv`).

6. **5-local_variables**  
   - Lists all **local variables**, **environment variables**, and **functions**.

7. **6-create_local_variable**  
   - Creates a **new local** variable named `BEST` with the value `School`.

8. **7-create_global_variable**  
   - Creates a **new global** variable named `BEST` with the value `School`.

9. **8-true_knowledge**  
   - Prints the result of adding `128` to the environment variable `TRUEKNOWLEDGE`.

10. **9-divide_and_rule**  
    - Prints the result of dividing the environment variable `POWER` by `DIVIDE`.

11. **10-love_exponent_breath**  
    - Displays `BREATH` to the power of `LOVE` (using shell arithmetic expansion).

12. **11-binary_to_decimal**  
    - Converts a binary number in the env variable `BINARY` into decimal.

13. **12-combinations**  
    - Prints all **possible combinations** of two lowercase letters, except `oo`, in alphabetical order.
    - One combination per line.
    - Script must contain maximum 64 characters.

14. **13-print_float**  
    - Prints a number (stored in `NUM`) with **two decimal places**.

15. **14-decimal_to_hexadecimal**  
    - Converts a decimal number (stored in `DECIMAL`) to base 16 (hexadecimal).

---

## Resources

- [Expansions](https://tldp.org/LDP/abs/html/abs-guide.html#EXPANSIONS)  
- [Shell Arithmetic](https://tldp.org/LDP/abs/html/ops.html)  
- [Shell Variables](https://tldp.org/LDP/abs/html/variables.html)  
- [Aliases](https://tldp.org/LDP/abs/html/aliases.html)  
- [Shell Initialization Files](https://www.gnu.org/software/bash/manual/bash.html#Bash-Startup-Files)  
- [man pages: `printenv`, `set`, `unset`, `export`, `alias`, `unalias`, `source`, `printf`]  

---

**Enjoy experimenting with shell variables, expansions, and aliases!**