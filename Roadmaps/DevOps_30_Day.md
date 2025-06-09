# ✅ DevOps Crash Course - 30 Day Plan

## 🎯 Project Goal

Host and manage a small website (Flask / Node.js / Static) on a cloud VPS with:
- [ ] Docker deployment
- [ ] GitHub Actions CI/CD
- [ ] HTTPS via Let's Encrypt
- [ ] SSH & firewall hardening
- [ ] Monitoring & logs
- [ ] Auto-backup script

---

## 🗓 Week 1: Foundations + Manual Deployment

### 📘 Key Topics
- [x] Ubuntu/Linux CLI basics (ssh, sudo, nano, systemctl)
- [ ] Git + GitHub
- [ ] Web server (Nginx)
- [ ] Domain + SSL (Let's Encrypt)

### 🛠 Action Plan
- [ ] Get a VPS (DigitalOcean, Linode, AWS Free Tier, etc.)
- [ ] Set up Nginx and UFW firewall
- [ ] Clone a sample app from GitHub
- [ ] Set up domain + SSL using Certbot

✅ **Outcome:** Public HTTPS site running via Nginx
**links** [[SSH]]

---

## 🐳 Week 2: Docker + SSH Automation

### 📘 Key Topics
- [ ] Docker & docker-compose
- [ ] Bash scripting
- [ ] Basic deployment automation

### 🛠 Action Plan
- [ ] Write a Dockerfile and docker-compose.yml
- [ ] Run your app using Docker locally
- [ ] Copy Docker setup to VPS and run containers
- [ ] Write a `deploy.sh` script to rebuild/restart containers

✅ **Outcome:** App runs in Docker, deployed via script

---

## 🚀 Week 3: CI/CD with GitHub Actions

### 📘 Key Topics
- [ ] GitHub Actions
- [ ] SSH Deploy
- [ ] Secrets & environment variables

### 🛠 Action Plan
- [ ] Create `.github/workflows/deploy.yml`
- [ ] Configure GitHub Actions to SSH into VPS
- [ ] On push, auto-build and deploy app
- [ ] *(Bonus)* Add build/test/lint steps

✅ **Outcome:** Push to GitHub = live deployment

---

## 🛡 Week 4: Monitoring, Backup & Hardening

### 📘 Key Topics
- [ ] Logs & monitoring (journalctl, docker logs, etc.)
- [ ] UptimeRobot
- [ ] SSH security best practices
- [ ] Cron-based backups

### 🛠 Action Plan
- [ ] Set up UptimeRobot or other monitoring
- [ ] Disable root SSH login, enforce key-based login
- [ ] Create a daily backup cron job (logs + DB)
- [ ] Send backups to remote or cloud storage

✅ **Outcome:** Monitored, secure, auto-backed-up live app

---

## 🧰 Bonus: Free Tools You Can Use

- [ ] Uptime Monitoring: [uptimerobot.com](https://uptimerobot.com)
- [ ] Cheap VPS: Hetzner, DigitalOcean, Oracle Cloud Free Tier
- [ ] SSL: [certbot.eff.org](https://certbot.eff.org)
- [ ] Sample App: Flask Example or static HTML+JS
