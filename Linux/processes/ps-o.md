# Common and Important `ps -o` Output Columns

The `ps` command in Linux allows you to view detailed information about running processes. The `-o` option enables you to specify which columns of information you'd like to display. Here are some of the **most common and important columns** you can use with `ps -o`:

---

## **1. PID (Process ID)**
- **Syntax:** `pid`
- **Description:** The unique identifier for each running process.
- **Example:**
    ```sh
    ps -eo pid,comm
    ```

## **2. PPID (Parent Process ID)**
- **Syntax:** `ppid`
- **Description:** The process ID of the parent process.
- **Example:**
    ```sh
    ps -eo pid,ppid,comm
    ```

## **3. UID (User ID)**
- **Syntax:** `uid`
- **Description:** The user ID (numeric value) of the user running the process.
- **Example:**
    ```sh
    ps -eo pid,uid,comm
    ```

## **4. EUID (Effective User ID)**
- **Syntax:** `euid`
- **Description:** The effective user ID of the process, considering any privilege escalation (e.g., `sudo`).
- **Example:**
    ```sh
    ps -eo pid,euid,comm
    ```

## **5. GID (Group ID)**
- **Syntax:** `gid`
- **Description:** The numeric ID of the group associated with the process.
- **Example:**
    ```sh
    ps -eo pid,gid,comm
    ```

## **6. EGID (Effective Group ID)**
- **Syntax:** `egid`
- **Description:** The effective group ID of the process, considering any group privilege changes.
- **Example:**
    ```sh
    ps -eo pid,egid,comm
    ```

## **7. TTY (Terminal Type)**
- **Syntax:** `tty`
- **Description:** The terminal associated with the process, if any (e.g., `tty1`, `pts/0`).
- **Example:**
    ```sh
    ps -eo pid,tty,comm
    ```

## **8. TIME (Cumulative CPU Time)**
- **Syntax:** `time`
- **Description:** The total CPU time consumed by the process.
- **Example:**
    ```sh
    ps -eo pid,time,comm
    ```

## **9. STAT (Process Status)**
- **Syntax:** `stat`
- **Description:** Current status of the process, where:
    - `R` = Running
    - `S` = Sleeping
    - `T` = Stopped
    - `Z` = Zombie
    - etc.
- **Example:**
    ```sh
    ps -eo pid,stat,comm
    ```

## **10. NI (Nice Value)**
- **Syntax:** `ni`
- **Description:** The nice value of the process, which affects its priority.
- **Example:**
    ```sh
    ps -eo pid,ni,comm
    ```

## **11. PRI (Priority)**
- **Syntax:** `pri`
- **Description:** The process’s priority level, determined by the OS scheduler.
- **Example:**
    ```sh
    ps -eo pid,pri,comm
    ```

## **12. CMD (Command)**
- **Syntax:** `cmd`
- **Description:** The full command line that started the process, including arguments.
- **Example:**
    ```sh
    ps -eo pid,cmd
    ```

## **13. COMM (Command Name)**
- **Syntax:** `comm`
- **Description:** The name of the command that started the process, without arguments.
- **Example:**
    ```sh
    ps -eo pid,comm
    ```

## **14. RSS (Resident Set Size)**
- **Syntax:** `rss`
- **Description:** The non-swapped physical memory (in kilobytes) used by the process.
- **Example:**
    ```sh
    ps -eo pid,rss,comm
    ```

## **15. VSZ (Virtual Memory Size)**
- **Syntax:** `vsz`
- **Description:** The total virtual memory used by the process (in kilobytes).
- **Example:**
    ```sh
    ps -eo pid,vsz,comm
    ```

## **16. START (Start Time)**
- **Syntax:** `start`
- **Description:** The time the process started.
- **Example:**
    ```sh
    ps -eo pid,start,comm
    ```

## **17. CPU (CPU Usage Percentage)**
- **Syntax:** `pcpu`
- **Description:** The percentage of CPU time used by the process.
- **Example:**
    ```sh
    ps -eo pid,pcpu,comm
    ```

## **18. MEM (Memory Usage Percentage)**
- **Syntax:** `pmem`
- **Description:** The percentage of physical memory used by the process.
- **Example:**
    ```sh
    ps -eo pid,pmem,comm
    ```

---

### **How to Use These Options Together**

You can combine multiple outputs to get detailed information. For example, to list processes with their **PID**, **memory usage**, **CPU usage**, and **command**, you can run:

```sh
ps -eo pid,pmem,pcpu,comm
```

## ps: 
**made by chatgpt**
