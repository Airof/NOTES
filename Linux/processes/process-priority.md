# Preview:
- **Lower nice values** (`-20`) = Higher priority
- **Higher nice values** (`19`) = Lower priority
- Use `ps -eo pid,ni,pri,comm` to check priorities
- Use `nice` to start a process with a priority
- Use `renice` to change priority of a running process

---
# 1.Understanding Process Priority
- **Nice Value (`nice`):** A user-controlled value that affects the process priority.
- **Scheduling Priority (`PR`):** The final priority assigned by the OS based on the nice value and other system factors.

|Priority Type	 |  Value Range               |
|----------------|----------------------------|
|Nice Value      |-20 (highest) to 19 (lowest)|
|Scheduling      | Priority	0 to 139          |

# 2.Checking Process Priorities

**Show all processes with priorities**
```bash
ps -eo pid,ni,pri,comm # -o> output 
```
important outputs:
- `pid` - Process ID
- `ppid` - Parent Process ID
- `uid` - User ID
- `time` - CPU Time
- `stat` - Process Status
- `ni` - Nice value
- `pri` - Priority
- `rss` - Resident Set Size (Memory used)
- `vsz` - Virtual Size (Memory used)
- `cmd` - Command line used to start the process

for detailed information see:
**[Common and Important ps -o Output Columns](ps-o.md)**

**Show priority of a specific process**
```bash
ps -o pid,ni,pri,comm -p <PID>
```

# 3.Changing Process Priority
You can adjust priority using the `nice` and `renice` commands

**Start a process with a specific priority**
```bash
nice -n <value> command
#EXAMPLE
nice -n -5 ./heavy_program #Runs heavy_program with higher priority(-5)
```
**Change priority of a running process**
```bash
renice -n <value> -p <PID>
#EXAMPLE:
renice -n 10 -p 1234 #Sets lower priority (10) for process 1234
```

# 4.Priority Scheduling in Linux
Linux uses **CFS (Completely Fair Scheduler)**, which prioritizes tasks based on:

- **Nice** value (user-defined)
- **CPU** time used
- **System** load
- **Process** type (real-time vs. normal)

|Type	            |Description         |	Priority Range|
|-------------------|--------------------|--------------------------|
|Real-time processes|	Used for critical system tasks (e.g., audio processing)	|0–99
|Normal processes	|Standard user programs (e.g., browsers, terminals)	|100–139

# 5.Important Notes on Priority
- **Only root** users can set a nice value **below 0**.
- `SIGSTOP`/`SIGCONT` can be used to pause/resume a process instead of changing priority.
- **High-priority tasks** (`-20` `nice value`) can slow down the system if not managed properly.
