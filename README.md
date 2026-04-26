# 🚀 DevSecOps Pipeline mit Kubernetes, n8n & Trivy

![CI/CD Pipeline](https://github.com/devops-inprogress/myapp/actions/workflows/deploy.yml/badge.svg)

## 📌 Projektübersicht

Dieses Projekt demonstriert eine automatisierte DevSecOps-Pipeline, die Sicherheitsprüfungen direkt in einen CI/CD-Prozess integriert.

Der Code wird mit Trivy gescannt, die Ergebnisse über n8n ausgewertet und basierend auf der Schwere automatisch entschieden, ob die Pipeline fortgesetzt oder gestoppt wird.

---

## 🧠 Architektur

Code Push (GitHub)
        ↓
GitHub Actions (CI/CD)
        ↓
Trivy Scan (Security Analyse)
        ↓
Webhook → n8n (Decision Engine)
        ↓
IF Logic (HIGH / CRITICAL)
        ↓
❌ Pipeline FAIL + Telegram Alert
oder
✅ Pipeline SUCCESS

---

## 👉 Tech Stack

## ⚙️ Technologien

- Kubernetes (k3s)
- Proxmox VE
- n8n (Workflow Automation)
- Trivy (Security Scanner)
- GitHub Actions (CI/CD)
- Cloudflare Tunnel
- Telegram API

---

## 🔐 Sicherheitslogik

| Severity        | Aktion                    |
|----------------|--------------------------|
| CRITICAL / HIGH | ❌ Pipeline wird gestoppt |
| LOW / MEDIUM    | ✅ Pipeline läuft weiter  |

---

## 📡 Beispiel Output

❌ Security issue found - failing pipeline  
📱 Telegram Alert ausgelöst  

oder  

✅ No blocking security issues

---

## 🧠 Learnings

- Aufbau eines Kubernetes Clusters (k3s)
- Integration von Security Scans in CI/CD
- Automatisierte Entscheidungslogik mit n8n
- Webhook-basierte Kommunikation
- Umsetzung eines Security Gates
