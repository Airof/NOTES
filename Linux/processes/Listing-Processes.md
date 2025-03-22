# Listing Running Processes
**using `ps`:**
```bash
ps # list all processes in the current tty
ps aux   # List all processes with details
ps -e    # Another format for listing all processes
ps -f   #shows more details
ps -u $USER  # Show processes owned by the current user
```
**Using `tops`**
```bash
top #pre-installed in most distros
htop # better visualized
btop # my prefered
```
using `pgrep` and `pidof`

```bash
pgrep zen #> 10925
pgrep -l zen #> 10925 zen

pidof zen #> 43434 43386 24791 11224 11216 11163 11074 11070 11010 10925
```
**process directories**
```bash
ls /proc # list process directories
cat /proc/1234/status  # Check details of a specific process
cat /proc/1234/cmdline # Check the command line that started a process
```


