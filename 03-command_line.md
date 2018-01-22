# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > * show current working directory path - `pwd`
> > * create a directory - `mkdir` 
> > * delete a directory - `rmdir`
> > * creating a file using touch command - `touch file_name`
> > * deleting a file - `rm` 
> > * renaming a file - `mv old_filename new_filename`
> > * listing hidden files - `ls -ld .?*` (list hidden files only)
> > * copying a file from one directory to another - `cp file_name file_path_of_new_directory`
> > * remove an empty directory - `rm -rf directory_name`
> > * list all files in directory - `ls` 
> > * change the working directory - `cd` 
> > * examine environment - `env`

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > * `ls` - list all files in current working directory
> > * `ls -a` - do not ignore files starting with . 
> > * `ls -l` - use long listing format 
> > * `ls -lh` - print file sizes in a human readable format 
> > * `ls -lah` - combines the functions of -l, -a, and -h
> > * `ls -t` - display newest files first 
> > * `ls -Glp` - long listing format, don't print group names, include indicator to directories 

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 1. `ls -1` - list one file per line 
> > 2. `ls -r` - reverse order while sorting 
> > 3. `ls -m` - list a comma separated list of entries 
> > 4. `ls -U` - do not sort, list entries in directory order 
> > 5. `ls -x` - list entries by lines instead of by columns 
> > 6. Bonus `ls -R` - list subdirectories recursively 

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` is used to create and execute commands from standard input, meaning it converts input from standard input into arguments for a command. `xargs` can be useful when used with other commands. For example, I can use `xargs` combined with the `find` command to find specific files. `xargs find -name "*.py"` would find all files in my current working directory that end in a .py extension. 

 

