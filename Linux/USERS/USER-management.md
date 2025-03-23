**Privilege Escalation**

- Switch user
```bash
su - username
```
- switch root
```bash
su
```
- Run command as another user
```bash
sudo -u username command
```


**User Management Commands**

- **view users**
    ```bash
    cat /etc/passwd # list all users
    who             #Show currently logged-in users
    whoami          #Show your current user:
    ```
- **Add Users** (need root access)
    ```bash 
    useradd username  # add user
    passwd username   # set password
    ```
    **flags for `useradd`:**
    |Flag    |Description   |
    |---------|------------| 
    |`-m`   |Creates a home directory (/home/username).    | 
    |`-d  /custom/home`	|Specifies a custom home directory.| 
    |`-s  /bin/bash`  |Sets the default shell for the user.| 
    |`-g  groupname`  |Assigns the user to a specific primary group.| 
    |`-G group1,group2`	|Adds the user to multiple secondary groups.| 
    |`-u 2001`|Sets a specific UID instead of the default.  | 
    |`-c "Full Name"`   |Adds extra user info (GECOS field).| 
    |`-e YYYY-MM-DD`  |Sets the account expiration date.| 

    **flags for `passwd`:**
    |Flag     |Description |
    |---------|------------|
    |`-d`       |**Delete** the user's password (disables password login).
    |`-e`       |**Expire** the password immediately (forces the user to change it on next login).
    |`-l`       |**Lock** the user’s password (disables login with password).
    |`-u`       |**Unlock** the user’s password.
    |`-S`       |**Shows** the password status of a user.
    |`-x DAYS`  |Sets the **maximum** number of days before password expiration.
    |`-n DAYS`  |Sets the **minimum** number of days before password can be changed.
    |`-w DAYS`  |Sets the **warning** period before password expiration.
    |`-i DAYS`  |Sets the **inactive** period before the account is disabled.

- **modify users**
    ```bash
    usermod <command> username
    usermod -d /new/home username # change user directory 
    sudo usermod -s /bin/bash username # change login shell
    sudo usermod -aG groupname username # add user to a group
    ```
- **delete users**
    ```bash
    sudo userdel username # Remove user (keeps home directory)
    sudo userdel -r username # Remove user and home directory
    ```









