# Terminal Practice

**`echo $SHELL`** returns,

- `/usr/bin/bash` on Git Bash
- `/bin/bash` on Ubuntu through WSL

Similar, but slight difference; even through the `usr/` directory does exist within Ubuntu on WSL.

===

**`pwd`** will tell you the current direcoty path you are currently in.  
The default/home (not root), for the terminal emulators being used are,  
`/home/tonch_liv` for ***Ubuntu***,  
`c/Users/ITTP` for ***Git Bash***,  
`C:\Users\ITTP` for ***Powershell***.  

**`ls`** will list the contents of the current directory, or the directory specified as an option after the command.  
**`cd`** is used to change directories.  

**Relative path** refers to,  
  A file or directory location relative to *where we currently are* in the file system.
**Absolute path**,  
  A file or directory location in *relation to the root* of the file system.

===

Linux is case sensitive as to commands and file names.  
The extension does not necessarily dictate the type of file; the content of the file does.  
The `file` command returns information on the type of file or directory.

Files and directories that begin with a period `.` indicate it is a hidden / configuration item. To view them in the return of the terminal, use the `-a` flag/option with `ls`.  

```bash
ls -a
```

===

manual pages are built to explain the commands on a system, what they do, how they are used, etc.  

===

`mkdir` to create a folder / directory.  
`rmdir` to delete a directory.  
`touch` preceeded before a file name creates a text file with the name.  
`mv` moves a file to a new destination.  

===

Editing files can be done within the terminal using **Vi**, a *CLI text editor*.  
**Insert** / **input** mode is as it says, where the user is able to enter content within a file.  
**Edit** mode allows you to make modifications like delete, copy, search, save, etc.  

initializing vi is as simple as following it up with the name of the file in question, `vi <file>`.  

===

[cheatsheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
