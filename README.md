# Shell

The shell is **a command line interpreter.** It can also execute other programs such as applications, scripts, and user programs (written in c or the shell programming language).

## Basic shell commands used in this project.

* `pwd` command is used to print the path of the current directory you're in.
 

* `cd` command is used to navigate through files or directories.
    cd options  | Functions
    ------------- | -------------
    `cd .` | represents current directory
    `cd ..`  | move one directory back (parent directory)
    `cd`  | move to the root directory
    `cd -` | move to the previous directory


* `ls` command is used to view (list) the content of a directory (current directory, by default).
   ls options  | Functions
    ------------- | -------------
    `ls -R`   | list all files (even in sub-directories)
    `ls -a`  | show the hidden files (even the ones starting with `.`)
    `ls -l` | list files in long format (detailed info)
    `ls -n` | show content with user and group IDs displayed numerically



* `cp` command is used to copy files from the current directory to another directory.
    * `cp *.html` copies all files ending with `.html`.
    * `cp [A-Z]*` copies all files which name start with an uppercase letter.
        * `*` matches one or more character, including no character.
    cp options | Functions
            ----------------  |  ------------
            `cp -r` | copy files/directories recursively.
            `cp -u` | copy only when the SOURCE file is newer than the destination file or when the destination file is missing.


* `mv` command is mainly used to move files, but it's also used to rename files.
   * `mv file1.txt /root/school` (moves `file1` to `school` directory).
   * `mv file1.txt file2.txt` (renames `file1` to `file2`).


* `touch` command is used to create one or multiple new files.


* `rm` command is used to delete files.
    rm options | Functions
    ---------- | ---------
    `rm -rf` | force delete files/directories and their content.


* `mkdir` command is used to create new directories.


* `rmdir` command is used to delete directories, but it only allows you to delete empty directories.


* `chmod u+x file` makes the file executable.


## **[Manual Pages](https://linuxcommand.org/lc3_man_page_index.php#file)**

