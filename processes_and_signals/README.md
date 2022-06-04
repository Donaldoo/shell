# Shell, processes and signals
**What is a PID?** A PID is an indetification number that is given to a *process* every time it starts.</br>
**What is a process?** A process is a running instance of a program. Each process has a unique PID, which changes everytime the process starts. (*Init* process always has the same PID, which is 1.) </br>
**What is a signal?** Signals are software interrupts. The two signals that can never be ignored are **SIGKILL** and **SIGSTOP**
####  ***Important commands***
* `ps`: (*Process status*) is used to display information about a running process. (PID, TTY, TIME, CMD)
* `pgrep`: Searches for processes currently running on the system, based on a complete or partial process name, or other specified attributes.
* `pkill`:  Sends a signal to one or more processes, using the same flexible selection methods as pgrep.
* `kill`: This command is used to terminate processes manually.
* `exit`: This command is used to exit from the current shell.
* `trap`: Allows you to catch signals and execute code when they occur.

#### *Scripts using important commands*
* [0-what-is-my-pid](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/0-what-is-my-pid) - Displays its own PID.
* [1-list_your_processes](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/1-list_your_processes) - Lists all running processes, including those which may not have TTY, in a hierarchy order.
* [2-show_your_bash_pid](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/2-show_your_bash_pid) - Previous command + displays lines containing the bash word, easier to get the PID of Bash process.
* [3-show_your_bash_pid_made_easy](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/3-show_your_bash_pid_made_easy) - Displays only the PID of the processes containing `bash`.
* [4-to_infinity_and_beyond](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/4-to_infinity_and_beyond) - Script that prints a message indefinitely every 2 seconds.
* [5-dont_stop_me_now](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/5-dont_stop_me_now) - Kills previous process.
* [6-stop_me_if_you_can](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/6-stop_me_if_you_can) - Stops process using pkill command.
* [7-highlander](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/7-highlander) - Prints `To infinity and beyond` indefinitely every 2 seconds and prints `I am invincible!!!` when it stops.
* [8-beheaded_process](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/8-beheaded_process) - Script that kills highlander.
* [10-process_and_pid_file](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/10-process_and_pid_file) - Creates the file `/var/run/myscript.pid` containing its PID, displays `To infinity and beyond` indefinitely, `I hate the kill command` when receiving a `SIGTERM` signal. `Y U no love me?!` when receiving a `SIGINT` signal, deletes the file `/var/run/myscript.pid` and terminates itself when receiving a `SIGQUIT` or `SIGTERM` signal.
* [11-manage_my_process](https://github.com/Donaldoo/shell/blob/main/processes_and_signals/11-manage_my_process) - Manages background process `manage_my_process`. Either starting, stopping or restarting the other process and creating a file storing its PID.
