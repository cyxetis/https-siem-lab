# 🔐 HTTPS-SIEM-Lab

> Local SIEM stack using **Zeek**, **Suricata**, **Filebeat**, and **Elasticsearch** — secured with **TLS** and **localhost-only** access.

---

## 🧱 Stack Overview

- **Elasticsearch 8.17.3** with TLS & Authentication enabled  
- **Filebeat** securely shipping logs over HTTPS  
- **Zeek** for passive traffic inspection  
- **Suricata** for signature-based IDS  
- **Systemd-managed services** with auto-restart  

---

## ⚙️ File Structure

├── elasticsearch.yml
├── kibana.yml
├── filebeat.yml
├── suricata.yaml
├── systemd/
│ ├── elasticsearch.service
│ ├── filebeat.service
│ └── ...
└── certs/
├── ca.crt
├── elasticsearch.crt
└── elasticsearch.key

---


---

## 🔐 Security Features

- ✅ HTTPS across all components  
- ✅ Local-only binding (`127.0.0.1`)  
- ✅ Role-based users (`elastic`, `filebeat_internal`)  
- ⚠️ **Default credentials should be rotated**

---

## 📦 Use Case

> Built for **Incident Response (IR)** training and **portfolio showcase** — demonstrating secure log collection, network traffic visibility, and SIEM component integration.

---

## 🛠️ Deployment Notes

- Runs **offline**, no external/cloud dependencies  
- All logs ingested from:
  - `/opt/zeek/logs/current/*.log`  
  - `/var/log/suricata/eve.json`  
- HTTPS certs generated with **Elastic cert tool**

---

## 💡 Next Plans

- Integrate **Kibana Dashboards**  
- Add **Ansible automation**  
- Tune custom **detection logic** (Zeek/Suricata)

---
