# Init files, variables and expansions
### [*Expansion*](http://linuxcommand.org/lc3_lts0080.php)
Every time we type a command in the terminal, bash performs several processes upon the text before it carries out our command. The process that makes a simple character sequence have a lot of meaning to the shell is called ***expansion***.
* **Pathname Expansion**
The mechanism by which *wildcards* work is called pathname expansion.
* **Tilde Expansion**
When tilde character (~) is used at the beginning of a word, it expands into the name of the home directory of the named user (if no user is named, prints name of the directory of the current user).
* **Arithmetic Expansion**
Arithmetic expansion can be used to perform simple integer arithmetic operations, and uses the form `$((expression))`
* **Brace Expansion**
With brace expansion we can create multiple text strings from a pattern containing braces. The brace expression may contain either a comma-separated list of strings, or a range of integers or single characters.
* **Parameter Expansion**
One of the parameter expansion capabilities has to do with the system's ability to store variables and to give each variable a name.
* **Command Substitution**
Command substitution allows us to use the output of a command as an expansion.
* **Quoting**
The shell provides a mechanism called *quoting* to selectively suppress unwanted expansions.
  
  * *Double Quotes*
      All the special characters inside double quotes used by the shell lose their special meaning and are treated as ordinary characters.
  * *Single Quotes*
      Suppress all expansions inside single quotes.
  * *Escaping Characters*
      We use escaping (backslash) to eliminate the special meaning of a character in a filename.



### [*Variables*](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_02.html)
Variables are in uppercase characters by convention. There are two types of variables:
* **Global variables** (Global variables or environment variables are available in all shells) 
`export NAME="value"` - create a new global/environment variable.
`printenv` - display environment variables.
`set` - displays and sets the names and values of environment variables.
`unset` -  remove the variable from the list of variables that shell tracks.
* **Local variables** (Local variables are only available in the current shell)
`NAME="value"` - create a new local variable.


### [*The alias Command*](http://www.linfo.org/alias.html)
The alias command makes it possible to launch any command or group of commands (separated by ;) options, by entering a pre-set string.
`alias p="pwd"` - create alias p for command pwd.
`unalias` - removes aliases previously set with the alias command.



#### *Other commands used in this project:*
`printf` - is used to display the given string, number or any other format specifier on the terminal window.

`source` - is used to read and execute the content of a file, passed as an argument in the current shell script.



### *Some combinations of commands used in this project:*
* [Combinations](https://github.com/Donaldoo/shell/blob/main/init_files_variables_and_expansions/12-combinations) - prints all possible combinations (one per line) of two letters, except `"oo"`, letters are lower case and alpha ordered, starting with "aa".
* [Odd](https://github.com/Donaldoo/shell/blob/main/init_files_variables_and_expansions/16-odd) - prints every other line from the input, starting with the first line.
* [Water_and_stir](https://github.com/Donaldoo/shell/blob/main/init_files_variables_and_expansions/17-water_and_stir) - adds the two numbers stored in the environment variables `WATER` and `STIR` and prints the result in base `bestchol`. (`WATER` is in base `water` and `STIR` is in base `stir.`)
