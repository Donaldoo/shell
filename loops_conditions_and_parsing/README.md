# Shell, loops conditions and parsing

# Loops, conditions and parsing
## *Loops*
A loop is a programming tool that enables the user to execute a set of commands repeatedly. In this project we will learn the following loops:
* [The for loop](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_09_01.html) - The for loop allows for specification of a list of values. A list of commands is executed for each value in the list.
* [The while loop](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_09_02.html) - The while loop keeps executing until the condition becomes false.
* [The until loop](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_09_03.html) - The until loop executes until the condition becomes true.


## *Condition statements*
* **if** - Represents the condition that you want to check.
* **then** - If the previous condition is true, then execute a specific command.
* **elif** - Is used to add an additional condition to your statement.
* **else** - If the previous conditions are false, then execute another command.
* **fi** - closes the “if, elif, else” statement
* **case** - Alternative to a multilevel if-elif-else statement. It enables you to match several values against one variable. </br> 
*Syntax*:

```
case word in
pattern1)
Statement(s) to be executed if pattern1 matches
;;
pattern2)
Statement(s) to be executed if pattern2 matches
;;
pattern3)
Statement(s) to be executed if pattern3 matches
;;
*)
Default condition to be executed
;;
esac
```

#### *Comparison Operators*

Integer comparision | String comparision | Arithmetic operators
:----- | :-------- | :------
**-eq** is equal to - if ["$a" -eq "$b" ] | **=** is equal to - if [ "$a" = "$b" ] | + plus
**-ne** is not equal to - if ["$a" -ne "$b" ] | **==** is equal to - if [ "$a" == "$b" ] | - minus
**-gt** is greater than - if ["$a" -gt "$b" ] | **!=** is not equal to - if [ "$a" != "$b" ] | * multiplication
**-ge** is greater than or equal to - if ["$a" -gt "$b" ] | **<** is less than, ASCII alphabetical order - if [[ "$a" < "$b" ]] | / division
**-lt** is less than - if ["$a" -lt "$b" ] | **>** is greater than, ASCII alphabetical order - if [[ "$a" > "$b" ]] | ** exponentiation
**-le** is less than or equal to - if ["$a" -le "$b" ] | **-z** string is null, has zero length |**%** modulo (returns the remainder of an integer
**<** is less than - (("$a" < "$b")) | |  division operation)
**<=** is less than or equal to - (("$a" <= "$b")) | 
**>** is greater than - (("$a" > "$b")) | 
**>=**  is greater than or equal to - (("$a" >= "$b")) | 


#### *Scripts using loops and conditions, some used for parsing through text.*

- [1-for_best_school](https://github.com/Donaldoo/shell/tree/main/loops_conditions_and_parsing) - Script that displays `Best School` 10 times using `for` loop.
- [2-while_best_school](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/2-while_best_school) - Script that displays `Best School` 10 times using `while` loop.
- [3-until_best_school](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/3-until_best_school) - Script that displays `Best School` 10 times using `until` loop.
- [4-if_9_say_hi](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/4-if_9_say_hi) - Script that displays "Best School" 10 times, but for the 9th iteration, displays `Best School` and then `Hi` on a new line.
- [5-4_bad_luck_8_is_your_chance](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/5-4_bad_luck_8_is_your_chance) Script that displays `bad luck` for the 4th loop iteration, `good luck` for the 8th loop iteration and `Best School` for any other loop iterations.
- [6-superstitious_numbers](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/6-superstitious_numbers) his script displays `bad luck from china` in the 4th loop iteration, `bad luck from japan` in the 9th loop iteration, `bad luck from italy` in the 17th loop iteration, and numbers for any other loop until the number 20.
- [7-clock](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/7-clock) Script that displays hours from 0 to 12 and minutes from 1 to 59.
- [8-for_ls](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/8-for_ls) Displays the content of the current directory in a list format where only the names after the dash are displayed.
- [9-to_file_or_not_to_file](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/9-to_file_or_not_to_file) Script that gives you information about the `school` file, and if it exists which type of file it is.
- [10-fizzbuzz](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/10-fizzbuzz) Script that displays numbers 1-100. Replaces any number with `FizzBuzz` for which are a multiple of both 3 and 5, `Fizz` for multiples of 3 and `Buzz` for multiples of 5. Any other numbers displayed as is.
- [11-read_and_cut](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/11-read_and_cut) Script that displays the content of the file `/etc/passwd` but only the username, user id and home directory path for the user.
- [12-tell_the_story_of_passwd](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/12-tell_the_story_of_passwd)  Script that displays each line of the `/etc/passwd` file as a message, with some words being variable strings taken from the 1-7th fields of each line from the mentioned file.
- [13-lets_parse_apache_logs](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/13-lets_parse_apache_logs) Script that displays the parsed `Apache logs` to show only the IP and HTTP_code using the `awk` command.
- [14-dig_the-data](https://github.com/Donaldoo/shell/blob/main/loops_conditions_and_parsing/14-dig_the-data) Script that displays the parsed `Apache logs` to show IP and HTTP_code using the `awk` command in the desending order sorted by occurence.
