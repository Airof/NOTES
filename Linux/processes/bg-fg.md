# Linux background and foreground process management    

**send a command background:**
```bash 
command &
#Example:
sleep 60 &
```
or use `ctrl+z` to suspend a process then
```bash
bg
```
**send a process foreground:**
```bash
fg #for all
fg %1 # for proc [1]
```
**Viewing Background Jobs:**
```bash 
jobs
```
**killing jobs:**
```bash
kill PID # use process ID
kill %1 # use the job number
```

see also [[nohup.md]]