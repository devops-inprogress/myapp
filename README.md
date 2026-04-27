# 🚀 DevSecOps Pipeline with Kubernetes, n8n & Trivy
![CI/CD Pipeline](https://github.com/devops-inprogress/myapp/actions/workflows/deploy.yml/badge.svg)

## 📌 Project Overview
This project demonstrates an automated DevSecOps pipeline that integrates security checks directly into a CI/CD process.
Code is scanned with Trivy, results are evaluated through n8n, and based on severity, the pipeline automatically decides whether to continue or stop.

---

## 🧠 Architecture
Code Push (GitHub)
        ↓
GitHub Actions (CI/CD)
        ↓
Trivy Scan (Security Analysis)
        ↓
Webhook → n8n (Decision Engine)
        ↓
IF Logic (HIGH / CRITICAL)
        ↓
❌ Pipeline FAIL + Telegram Alert
or
✅ Pipeline SUCCESS

---

## 👉 Tech Stack
## ⚙️ Technologies
- Kubernetes (k3s)
- Proxmox VE
- n8n (Workflow Automation)
- Trivy (Security Scanner)
- GitHub Actions (CI/CD)
- Cloudflare Tunnel
- Telegram API

---

## 🔐 Security Logic
| Severity        | Action                    |
|----------------|--------------------------|
| CRITICAL / HIGH | ❌ Pipeline stops         |
| LOW / MEDIUM    | ✅ Pipeline continues     |

---

## 📡 Example Output
❌ Security issue found - failing pipeline  
📱 Telegram Alert triggered  
or  
✅ No blocking security issues

---

## 🧠 Learnings
- Building a Kubernetes cluster (k3s)
- Integrating security scans into CI/CD
- Automated decision logic with n8n
- Webhook-based communication
- Implementation of a security gate
