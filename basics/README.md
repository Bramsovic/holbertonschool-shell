# Project: Shell Basics

This project is about learning the basics of navigation and file manipulation on **Linux**, through simple **bash** scripts. Each script addresses a specific objective, described in the following sections.

## Repository Contents

- **0-current_working_directory**  
  Prints the absolute path of the current working directory.

- **1-listit**  
  Displays the list of files and folders in the current directory.

- **2-bring_me_home**  
  Changes the current working directory to the user’s home directory.  
  > *Hint:* Do not use environment variables such as `$HOME`.

- **3-listfiles**  
  Displays the contents of the current directory in long format (type, permissions, size, date, etc.).

- **4-listmorefiles**  
  Displays all contents of the current directory, including hidden files (those starting with a `.`), in long format.

- **5-listfilesdigitonly**  
  Displays all files, including hidden files, in long format **with numeric user and group IDs**.

- **6-firstdirectory**  
  Creates a directory named `my_first_directory` in the `/tmp` directory.

- **7-movethatfile**  
  Moves the file `betty` from `/tmp` to `/tmp/my_first_directory/`.

- **8-firstdelete**  
  Deletes the file `betty` in `/tmp/my_first_directory/`.

- **9-firstdirdeletion**  
  Deletes the directory `my_first_directory` in `/tmp`.

- **10-back**  
  Changes the working directory to the **previous** one (i.e., the one you came from).

- **11-lists**  
  Displays the list of **all** files (including hidden ones) in long format for:
  1. the current directory,
  2. the parent directory,
  3. and the `/boot` directory.

- **12-file_type**  
  Prints the type of the file `iamafile` located in `/tmp`.

- **13-symbolic_link**  
  Creates a symbolic link named `__ls__` to `/bin/ls`, in the current working directory.

- **14-copy_html**  
  Copies all `.html` files from the current working directory to its parent directory **only** if they do not already exist there, or if the local version is newer.

- **15-lets_move**  
  Moves all files beginning with an uppercase letter (`A` to `Z`) to the `/tmp/u` directory.  
  > *Note:* The directory `/tmp/u` will already exist.

- **16-clean_emacs**  
  Deletes all files in the current working directory that end with the `~` character.  
  > *Often used to clean up temporary Emacs files.*

- **17-tree**  
  Creates the directories `welcome/`, `welcome/to/`, and `welcome/to/school` in the current directory, using **only two lines** (and thus only two spaces) in the script.

## Rules and Requirements

1. **Allowed editors**: `vi`, `vim`, `emacs`.  
2. **Scripts tested on**: Ubuntu 22.04 LTS.  
3. **Each script must be exactly two lines**:  
   - The command `wc -l <script>` must return `2`.  
   - The first line **must** be `#!/bin/bash`.  
4. All files must end with a **newline**.  
5. Scripts must be **executable**:  
   ```bash
   chmod u+x <filename>
   ```
6. **Usage of** backticks (\`), `&&`, `||`, **or** `;` **is forbidden**.

## Useful Resources

- [What Is “The Shell”?](https://linuxcommand.org/lc3_lts0010.php)  
- [Navigation](https://linuxcommand.org/lc3_lts0020.php)  
- [Looking Around](https://linuxcommand.org/lc3_lts0030.php)  
- [A Guided Tour](https://linuxcommand.org/lc3_lts0040.php)  
- [Manipulating Files](https://linuxcommand.org/lc3_lts0050.php)  
- [Working With Commands](https://linuxcommand.org/lc3_lts0060.php)  
- [Reading Man pages](https://linuxcommand.org/lc3_man_pages/man1.html)  
- [Keyboard shortcuts for Bash](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#Command-Line-Editing)  
- [LTS (Long Term Support)](https://wiki.ubuntu.com/LTS)  
- [Shebang](https://en.wikipedia.org/wiki/Shebang_(Unix))  

For more information on each command:

- `man` or `help` (e.g., `man ls`, `help cd`, etc.)  
- Online documentation for *User commands*, *System calls*, *Library functions*, etc.

## Frequently Asked Questions

- **What does RTFM mean?**  
  *Read The Fine Manual* — an invitation to consult official documentation.

- **What is the difference between a terminal and a shell?**  
  - A **terminal** is the interface (physical or software) used to type commands and display output.  
  - A **shell** (e.g., `bash`, `zsh`) is the program that interprets the commands you enter.

- **How do I use command history?**  
  - Press `↑` to browse history, use `history` to list commands, etc.

- **What is the difference between the root directory (`/`) and the root user’s home directory (`/root`)?**  
  - `/` is the root of the entire filesystem.  
  - `/root` is the **home directory of the root user**. For a normal user, it’s `/home/username`.

- **What’s a symbolic link vs. a hard link?**  
  - A **symbolic link** points to another file path (like a shortcut).  
  - A **hard link** shares the same inode as the target file.

## License

This project is provided by Holberton School as part of the **Shell** curriculum.  
You are free to use it and adapt it as you see fit.

---

**Have fun and enjoy exploring these exercises!**