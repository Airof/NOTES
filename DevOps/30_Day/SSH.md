
## Basic connection
```bash
ssh user@Server_ip
#eg
ssh git@github.com

```

## 🛠 How to Generate an SSH Key
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

| `-t rsa`  | Key type: RSA (most common)                        |
| --------- | -------------------------------------------------- |
| `-b 4096` | Key size: 4096 bits (more secure than 2048)        |
| `-C`      | Comment (helps identify the key, often your email) |
