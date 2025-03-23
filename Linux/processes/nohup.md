# `nohup` (No Hangup) in Linux

`nohup` is a command that allows a process to **continue running in the background** even after the user logs out or closes the terminal.

```bash
nohup command [arguments] &
```
- `nohup` prevents the command from being terminated when the shell session ends.

- The `&` at the end runs the command in the background.

## What If You Forget &?

If you accidentally run nohup without &, you can still send the process to the background:

- 1️⃣ Pause the process with Ctrl + Z.
- 2️⃣ Move it to the background:
    ```bash
    bg
    ```
- 3️⃣ Disassociate it from the terminal:
    ```bash
    disown
    ```

## `nohup` creates a file by default

If `nohup` is used **without redirecting output**, it creates a file named `nohup.out` in the current directory.

This file stores both standard output (**stdout**) and standard error (**stderr**).

- to redirect the output
    ```bash
    nohup command > output.log 2>&1 & # send both stdout and stderr to output.log

    nohup command > output.log 2>error.log # sends errors to a diffrent directory
    ```
