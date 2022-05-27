# I/O Redirections and filters.
### *Input/Output Redirections* "<" ">"
Commands accept input from a facility called ***standard input*** which by default is the keyboard, but it can be redirected. To redirect standart input we use the character "**<**".
Command line programs send their results to a facility called ***standard output*** which by default is the terminal, but just like standard input it can be redirected. To redirect standard output we use the character "**>**".


### *Pipelines* "|"
To connect two commands together we use ***pipelines***. With pipelines the standard output of the first command becomes the input for the next command.


### *Filters*
***Filters*** are programs that take the text from a file or produced by another format as their standard input, transform it to a meaningful format and then returns it as standard output.
Used filters in this project are:
* `cat`: Displays the text of a file line by line.


* `head`: Displays the first lines of a text file. If the number of lines is not specified **(-n)** then by default prints 10 lines.


* `tail`: Works the same way as head but it displays the last lines instead of the first lines.
  * `tail -n +2`: Displays all lines from line 2 to the end.


* `sort`: By default sorts the lines alphabetically [a-z] but it has other options:

sort options | functions 
:------------ | :---------
-n | Compare by string numerical value.
-r | Reverse the result of comparisons.
-k | Sort by key.
-V | Natural sort of (version) numbers within text.
-f | Fold lower case to upper case characters.


* `cut`: This command is used to extract a given number of characters or columns from a file.

cut options | functions
:---------- | :--------
-c | Select only these characters.
-d | Set delimiter.
-f | Select only these fields, also prints any line that contains no delimiter.


* `uniq`: Removes duplicate lines (it can only remove continuous duplicate lines but we can fix this by using pipelines).

uniq options | functions
:----------- | :--------
-u | Only prints unique lines.
-d | Only prints duplicated lines, one per group.
-c | Counts how many times lines are repeated and shows it as a numerical value before each line


* `grep`: Search a particular information from a text file.
``` 
grep [options] pattern [path] 
```

grep options | functions
:----------- | :--------
-v | Prints all lines that do not match the pattern.
-i | Ignores, case for matching.


* `tr`: This command is used for translating or deleting characters.
  * `tr -d [SET1]` - deletes characters in SET1


* `wc`: Gives the number of lines, words and characters in a text file.
  * `wc -l` Counts lines.
 

* `rev`: This command is used to reverse the lines characterwise.


### *Special characters*
Special characters are characters that do not have a literal meaning. They carry special instructions.

Character | Description
--------- | -----------
" " | *Whitespace* - space, tab, new line, carriage return.
'' | *Single quotes* - protect the text to have literal meaning.
"" | *Double quotes* - do not allow the text to be split.
\ | *Backslash* -  prevents the next character from being interpreted as a special character.
&#35; | *Comment* - notes of explanation, not processed by the shell.
&#124; | *Pipe* - send the output from one command to the input of another command.
; | *Command separator* - used to separate multiple commands that are on the same line.
~ | "Tilde" - home directory.

### *Some combinations of commands used in this project:*
* [.gif](https://github.com/Donaldoo/shell/blob/main/io_redirections_and_filters/24-gifs) - Lists all regular files (including hidden files) with a `.gif` extension in the current directory and all its sub-directories (one file per line). File names are displayed without their extensions. Files are sorted by byte values, but case-insensitive.
* [The biggest fan](https://github.com/Donaldoo/shell/blob/main/io_redirections_and_filters/26-the_biggest_fan) - Parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests. Most active IP (host) should be displayed at the top.
