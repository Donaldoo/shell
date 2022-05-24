# Shell Permissions
Each file and directory is given access rights for the owner of the file **(u)**, the members of a group of related users **(g)**, and everyone else **(o)**. Those rights are: read a file **(*r*)**, write a file **(*w*)** and execute a file **(*x*)**.
To view file rights use command `ls -l file_name`.

## Commands used in this project:

* `id -un` command is used to print the effective username of the current user.


* `group` command is used to list the groups a user belongs to.


* `su` command is used to temporarily become the superuser, also to change users if it used like:
  * `su user1` changes user to user1.


* `chown` command is used to change file ownership **(change owner)**.
   * `chown user1 text` - changes the owner to `user1` for the file `text`.
   * `chown user1:grp_owner1 text` - changes the owner to `user1` and the group owner to `grp_owner1` for the file `text`.
   * `chown -h user1 text` - changes the owner of the symbolic link `text` to `user1`


* `chgrp` command is used to change a file's group ownership. **(change group)**
   * `chgrp new_group text` - changes the group ownership of the file `text` to `new_group`


* `chmod` command is used to change file acces rights **(change mode)**.

```
rwx = 111 in binary = 7                   -wx = 011 in binary = 3
rw- = 110 in binary = 6                   -w- = 010 in binary = 2
r-x = 101 in binary = 5                   --x = 001 in binary = 1
r-- = 100 in binary = 4
```

**Value** | **Permissions meaning**
--------- | -----------------------
007 | Owner **(u)** and group **(g)** have no permissions at all, other users **(o)** have all permissions **(------rwx)**
753 | **u** has all permissions, **g** has read and execute permissions, **o** have write and execute permissions **(rwxr-x-wx)**
754 | **u** has all permissions, **g** has read and execute permissions, **o** have read permissions **(rwxr-xr--)**

The symbolic mode format is [ugoa]+[rwxX], or a single letter from [ugo] set. You can also give mulptiple symobilic modes by separating them by commas. ***(x) execute, (X) execute only if the file is a directory or already has execute permission.***

### Directory permissions

`chmod` command can also be used to give or remove permissions for directories. We use the same octal notation to set permission, but **r, w, x** attributes are different.
* **r** - Allows the files of the directory to be listed.
* **w** - Allows files to be created within the directory, deleted or renamed.
* **x** - Allows a directory to be entered.


## [Manual Pages](http://linuxcommand.org/lc3_man_page_index.php#file)


