# Linux Process Management

## Objective

Practice identifying running processes using the Linux `ps` command.

## Process Listing

Command:
ps

Result:
PID TTY          TIME CMD
19864 pts/2      00:00:00 /da
24642 pts/2      00:00:00 ps

## Analysis

- PID identifies each running process.
- TTY shows the terminal associated with the process.
- TIME shows the CPU time used by the process.
- CMD shows the command or process name.

The `ps` command also appears in its own process listing because it is itself a running process.

## Conclusion

This exercise demonstrated basic Linux process identification using `ps` and showed how to read process ID, terminal, CPU time, and command in

## Detailed Process Listing

Command:
ps -ef

The detailed process listing shows the user, PID, parent PID (PPID), CPU information, terminal, CPU time, and command.

The Bash shell was identified as PID 19864, while the `ps -ef` command appeared as its child process.

## Process Tree

Command:
pstree

Result:
?───?───/data/data/com.termux/files/usr/bin/bash─+++

The process tree output is limited in the Termux/Android environment.

## Conclusion

The process inspection exercises demonstrated how to identify and inspect running processes using `ps`, `ps -ef`, and `pstree`.
