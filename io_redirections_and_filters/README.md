# Project: Shell I/O Redirections and Filters

This project focuses on redirecting input and output in **Linux**, as well as using filters and special characters to manipulate data streams. Each **bash** script is exactly two lines, with `#!/bin/bash` on the first line.

## Table of Contents
1. [Learning Objectives](#learning-objectives)  
2. [Requirements](#requirements)  
3. [Project Structure](#project-structure)  
4. [Script Descriptions](#script-descriptions)  
5. [Resources](#resources)

---

## Learning Objectives

By the end of this project, you should be able to explain, without Google or external help:

- **Shell, I/O Redirection**  
  - What commands like `head`, `tail`, `find`, `wc`, `sort`, `uniq`, `grep`, `tr` do  
  - How to redirect standard output/input from/to files  
  - How to pipe the output of one program into another  
  - How to chain commands and filters with redirections  

- **Special Characters**  
  - What special characters are in the shell (spaces, quotes, backslash, comment `#`, pipe `|`, command separator `;`, tilde `~`, etc.)  
  - How and when to use them correctly  

- **Other Man Pages**  
  - Displaying lines of text (`echo`)  
  - Concatenating files and printing to standard output (`cat`)  
  - Reversing a string (`rev`)  
  - Removing sections from each line (`cut`)  
  - What `/etc/passwd` and `/etc/shadow` files are, and their formats  

---

## Requirements

1. **Allowed editors**: `vi`, `vim`, `emacs`.  
2. **Scripts tested on**: Ubuntu 20.04 LTS.  
3. **Each script must have exactly 2 lines** (i.e., `wc -l file` returns `2`).  
4. **Files must end with a newline**.  
5. **First line of each script**: `#!/bin/bash`.  
6. A `README.md` at the project root describing what each script does.  
7. **No** backticks (\`), `&&`, `||`, or `;` allowed.  
8. All scripts must be **executable** (`chmod u+x filename`).  
9. **No** `sed` or `awk` usage is allowed.  

---

## Project Structure

```
io_redirections_and_filters
├── 0-hello_world
├── 1-confused_smiley
├── 2-hellofile
├── 3-twofiles
├── 4-lastlines
├── 5-firstlines
├── 6-third_line
├── 7-file
├── 8-cwd_state
├── 9-duplicate_last_line
├── 10-no_more_js
├── 11-directories
├── 12-newest_files
├── 13-unique
├── 14-findthatword
├── 15-countthatword
├── 16-whatsnext
├── 17-hidethisword
├── 18-letteronly
├── 19-AZ
├── 20-hiago
├── 21-reverse
├── 22-users_and_homes
└── README.md
```

---

## Script Descriptions

1. **0-hello_world**  
   Prints `Hello, World` followed by a new line.

2. **1-confused_smiley**  
   Displays a confused smiley: `"(Ôo)'`.

3. **2-hellofile**  
   Displays the content of the file `/etc/passwd`.

4. **3-twofiles**  
   Displays the content of `/etc/passwd` and `/etc/hosts`.

5. **4-lastlines**  
   Displays the **last 10 lines** of `/etc/passwd`.

6. **5-firstlines**  
   Displays the **first 10 lines** of `/etc/passwd`.

7. **6-third_line**  
   Prints only the **third line** of the file `iacta`.

8. **7-file**  
   Creates a file named exactly `\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)` containing the text `Best School`.

9. **8-cwd_state**  
   Writes the output of `ls -la` into `ls_cwd_content`. Overwrites if it exists, creates if it doesn’t.

10. **9-duplicate_last_line**  
    Duplicates the **last line** of the file `iacta`.

11. **10-no_more_js**  
    Deletes all regular files with a `.js` extension (in current directory and subfolders).

12. **11-directories**  
    Counts the number of **directories and sub-directories** in the current directory (excluding `.` and `..`).

13. **12-newest_files**  
    Displays the **10 newest files** in the current directory, one per line, sorted newest to oldest.

14. **13-unique**  
    Reads a list of words from stdin and prints only the words that appear **exactly once**, sorted.

15. **14-findthatword**  
    Displays lines containing the pattern `root` from `/etc/passwd`.

16. **15-countthatword**  
    Displays the **number of lines** that contain the pattern `bin` in `/etc/passwd`.

17. **16-whatsnext**  
    Displays lines containing `root` and the **3 lines after** them in `/etc/passwd`.

18. **17-hidethisword**  
    Displays all lines in `/etc/passwd` that **do not** contain `bin`.

19. **18-letteronly**  
    Displays all lines of `/etc/ssh/sshd_config` that **start with a letter** (uppercase or lowercase).

20. **19-AZ**  
    Replaces all characters `A` and `c` in input with `Z` and `e`, respectively.

21. **20-hiago**  
    Removes all letters `c` and `C` from the input.

22. **21-reverse**  
    Reverses its input string.

23. **22-users_and_homes**  
    Based on `/etc/passwd`, displays all users and their home directories, sorted by username.

---

## Resources

- **Commands**  
  - [head](https://man7.org/linux/man-pages/man1/head.1.html), [tail](https://man7.org/linux/man-pages/man1/tail.1.html), [find](https://man7.org/linux/man-pages/man1/find.1.html), [wc](https://man7.org/linux/man-pages/man1/wc.1.html), [sort](https://man7.org/linux/man-pages/man1/sort.1.html), [uniq](https://man7.org/linux/man-pages/man1/uniq.1.html), [grep](https://man7.org/linux/man-pages/man1/grep.1.html), [tr](https://man7.org/linux/man-pages/man1/tr.1.html), [rev](https://man7.org/linux/man-pages/man1/rev.1.html), [cut](https://man7.org/linux/man-pages/man1/cut.1.html)  
- **Files**  
  - `/etc/passwd`, `/etc/shadow`  
- **Shell and Redirection**  
  - [Shell I/O Redirection](http://linuxcommand.org/lc3_lts0070.php)  
  - [Special Characters](https://tldp.org/LDP/abs/html/special-chars.html)

---

**Happy scripting and keep exploring shell redirections!**