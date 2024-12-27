# Project: Shell Permissions

This project focuses on learning and practicing file permissions on **Linux**. You’ll create various **bash** scripts that handle permission changes, ownership changes, and more. Each script is exactly **two lines long**, with `#!/bin/bash` as the first line.

## Table of Contents
1. [Learning Objectives](#learning-objectives)  
2. [Requirements](#requirements)  
3. [Project Structure](#project-structure)  
4. [Script Descriptions](#script-descriptions)  
5. [Resources](#resources)  
6. [FAQ](#faq)

---

## Learning Objectives

By the end of this project, you should be able to explain, without external help:

- **Permissions**  
  - What the commands `chmod`, `sudo`, `su`, `chown`, `chgrp` do  
  - How to represent file permissions as digits (owner, group, other)  
  - How to change permissions, owner, and group of a file  
  - Why a normal user cannot `chown` a file  
  - How to run a command with root privileges  
  - How to become the superuser or change user identity  

- **Other topics**  
  - How to create a user  
  - How to create a group  
  - How to print real and effective user and group IDs (`id`)  
  - How to print the groups a user is in (`groups`)  
  - How to print the effective user ID (`whoami`)

---

## Requirements

1. **Allowed editors:** `vi`, `vim`, `emacs`.
2. **Tested on**: Ubuntu 22.04 LTS.
3. **Scripts are exactly 2 lines** (the command `wc -l filename` returns `2`).
4. **All files must end with a newline**.
5. **First line of each file**: `#!/bin/bash`
6. **A `README.md` file** at the root of this project folder, describing what each script does.
7. **No use of** backticks `` ` ``, `&&`, `||`, or `;` in the scripts.
8. **All scripts must be executable**: `chmod u+x filename`.
9. **Tasks 3 / 13 / 14 / 15 / 16** must be **present inside the sandbox** (`/tmp`) to be corrected.

---

## Project Structure

```
permissions
├── 0-iam_betty
├── 1-who_am_i
├── 2-groups
├── 3-new_owner
├── 4-empty
├── 5-execute
├── 6-multiple_permissions
├── 7-everybody
├── 8-James_Bond
├── 9-John_Doe
├── 10-mirror_permissions
├── 11-directories_permissions
├── 12-directory_permissions
├── 13-change_group
├── 14-change_owner_and_group
├── 15-symbolic_link_permissions
├── 16-if_only
└── README.md
```

---

## Script Descriptions

> **Note**: Each script has **exactly 2 lines**. The first line is the **shebang**:  
> `#!/bin/bash`

1. **0-iam_betty**  
   - Switches the current user to `betty`.  
   - Assumes the user `betty` exists on the system.

2. **1-who_am_i**  
   - Prints the **effective** username of the current user.  

3. **2-groups**  
   - Prints all the groups the current user is part of.  

4. **3-new_owner**  
   - Changes the owner of the file `hello` to `betty`.  
   - Must be run with root privileges (e.g., `sudo`).  

5. **4-empty**  
   - Creates an **empty file** called `hello`.  

6. **5-execute**  
   - Adds **execute** permission to the **owner** of the file `hello`.  

7. **6-multiple_permissions**  
   - Adds execute permission to owner and group owner of `hello`.  
   - Adds read permission to **other** users.  

8. **7-everybody**  
   - Adds execution permission for **owner**, **group**, and **others** on `hello`.  
   - **No commas** are allowed in the command.  

9. **8-James_Bond**  
   - Sets permissions for `hello` to:  
     - **Owner**: no permissions  
     - **Group**: no permissions  
     - **Others**: all permissions (rwx)  
   - **No commas** are allowed.  

10. **9-John_Doe**  
    - Sets the mode of `hello` to `-rwxr-x-wx`.  
    - **No commas** are allowed.  

11. **10-mirror_permissions**  
    - Sets the mode of `hello` to be the **same** as the file `olleh`.  
    - Uses existing permissions on `olleh` as a template.  

12. **11-directories_permissions**  
    - Adds **execute** permission to all subdirectories of the current directory (for owner, group, and others).  
    - **Regular files** should remain unchanged.  

13. **12-directory_permissions**  
    - Creates a directory named `my_dir` with permissions `751`.  
      - `7` (owner = rwx),  
      - `5` (group = r-x),  
      - `1` (others = --x).  

14. **13-change_group**  
    - Changes the **group owner** of the file `hello` to `school`.  
    - File `hello` must be in the same working directory.  
    - Must be present in `/tmp` for the checker.  

15. **14-change_owner_and_group**  
    - Changes the **owner** to `vincent` and the **group owner** to `staff` for **all files and directories** in the current working directory.  
    - Must be present in `/tmp` for the checker.  

16. **15-symbolic_link_permissions**  
    - Changes the **owner** and **group owner** of the symbolic link `_hello` to `vincent` and `staff`, respectively.  
    - `_hello` is a symbolic link pointing to `hello`.  

17. **16-if_only**  
    - Changes the **owner** of the file `hello` to `vincent` **only** if it is currently owned by `guillaume`.  
    - If `hello` is not owned by `guillaume`, script does nothing.  

---

## Resources

- **Permissions**  
  - [chmod](https://man7.org/linux/man-pages/man1/chmod.1.html)  
  - [sudo](https://man7.org/linux/man-pages/man8/sudo.8.html)  
  - [su](https://man7.org/linux/man-pages/man1/su.1.html)  
  - [chown](https://man7.org/linux/man-pages/man1/chown.1.html)  
  - [chgrp](https://man7.org/linux/man-pages/man1/chgrp.1.html)  
- **IDs and Groups**  
  - [id](https://man7.org/linux/man-pages/man1/id.1.html)  
  - [groups](https://man7.org/linux/man-pages/man1/groups.1.html)  
  - [whoami](https://man7.org/linux/man-pages/man1/whoami.1.html)  
- **User & Group Management**  
  - [adduser](https://man7.org/linux/man-pages/man8/adduser.8.html)  
  - [useradd](https://man7.org/linux/man-pages/man8/useradd.8.html)  
  - [addgroup](https://man7.org/linux/man-pages/man8/addgroup.8.html)  

---

## FAQ

1. **Why can’t a normal user `chown` a file?**  
   - Only `root` can change ownership of files. Non-root users can’t take ownership of files they don’t already own.

2. **How do I run a command as `root` or another user?**  
   - Use `sudo <command>` to run a command with root privileges.  
   - Use `su <username>` to switch to another user (if you have the password).

3. **What are symbolic links, and how do they differ from hard links?**  
   - A **symbolic link** (`ln -s target link_name`) is like a shortcut pointing to another file path.  
   - A **hard link** shares the same inode as the target file, which can have implications when deleting or moving files.

4. **How do I create a group or user?**  
   - `adduser <name>` or `useradd <name>` for creating a user.  
   - `addgroup <group_name>` for creating a group.

5. **How do I check my own user or group information?**  
   - `whoami` prints your effective username.  
   - `id` prints real/effective user and group IDs.  
   - `groups` prints the groups you belong to.

---

**Enjoy practicing your permissions skills!**