**Listing Available Signals**
```bash 
kill -l
```

## Commonly Used Signals

Signal	|Number	|Description
---------|:----------:|---------
SIGHUP |	1	|Hangup – Reloads config files or restarts a process
SIGINT |	2	|Interrupt – Stops process (like Ctrl + C)
SIGQUIT|	3	|Quit – Stops process and dumps core
SIGKILL|	9	|Forcefully kills a process (cannot be ignored)
SIGTERM|	15  |Gracefully terminates a process (default for kill)
SIGSTOP|	19  |Suspends a process (like Ctrl + Z, cannot be ignored)
SIGCONT|	18  |Resumes a stopped process
SIGTSTP|	20  |Suspends a process (like Ctrl + Z, can be continued with fg or bg)
___
<br>

## Sending Signals to Processes
**Kill a Process by PID**
```bash
kill -9 1234  # Force kill (SIGKILL)
kill -15 1234 # Graceful termination (SIGTERM, default)
kill -2 1234  # Simulate Ctrl + C (SIGINT)
```
**Kill a Process by Name**
```bash 
pkill -9 firefox  # Kill all Firefox processes
pkill -HUP nginx  # Reload Nginx config
```
**Kill All Processes of a User**
```bash
killall -u username
```
### Managing Suspended Processes
Suspend a Process
```bash
kill -STOP 1234
```
or use `Ctrl + Z` in the terminal.
Resume a Suspended Process
```bash
kill -CONT 1234
```
or use `fg` or `bg` to bring it back. (for more information read bg-fg.md)

[read signals.md](bg-fg.md)


### extra :
#### **list of all of signals base on my HW&SW**
Signal	    |Description
|-----------|--------------|
HUP (1)	    |Hangup – Reloads config files or restarts a process.
INT (2)	    |Interrupt – Stops a process (like Ctrl + C).
QUIT (3)	|Quit – Stops a process and dumps core.
ILL (4)	    |Illegal instruction – Stops process due to bad CPU instruction.
TRAP (5)	|Trace/breakpoint trap (used for debugging).
IOT (6)	    |Abort signal from abort().
BUS (7)	    |Bus error (misaligned memory access).
FPE (8)	    |Floating-point exception.
KILL (9)	|Forcefully kills a process (cannot be ignored).
USR1 (10)	|User-defined signal 1.
SEGV (11)	|Segmentation fault (invalid memory access).
USR2 (12)	|User-defined signal 2.
PIPE (13)	|Broken pipe (writing to a closed pipe).
ALRM (14)	|Alarm signal from alarm().
TERM (15)	|Gracefully terminate (default for kill).
STKFLT (16)	|Stack fault (not used on many architectures).
CHLD (17)	|Sent when a child process terminates.
CONT (18)	|Continue a stopped process.
STOP (19)	|Stop a process (cannot be ignored).
TSTP (20)	|Stop a process (can be resumed with fg or bg).
TTIN (21)	|Background process tries to read input.
TTOU (22)	|Background process tries to write output.
URG (23)	|Urgent condition on socket.
XCPU (24)	|CPU time limit exceeded.
XFSZ (25)	|File size limit exceeded.
VTALRM (26)	|Virtual alarm clock.
PROF (27)	|Profiling timer expired.
WINCH (28)	|Window resize signal.
POLL (29)	|Pollable event (SysV equivalent of SIGIO).
PWR (30)	|Power failure (system-dependent).
SYS (31)	|Bad system call. 
