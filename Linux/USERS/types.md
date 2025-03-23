# types of users

1. **Root User (`root`)**
    - Superuser with unrestricted access to the system.
    - UID = `0`
    - Can execute any command and modify system files.
    - Example: `su` to switch to root.

2. **Regular Users**
    - Created by administrators.
    - Have limited permissions.
    - Store personal files in `/home/username/`.

3. **System Users (Service Accounts)**
   - Created for running system services (e.g., `www-data` for Apache).
   - Typically have no shell access (`/usr/sbin/nologin` or `/bin/false`).