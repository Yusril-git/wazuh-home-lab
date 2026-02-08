HEAD
# wazuh-home-lab
Wazuh + Suricata home lab attack &amp; detection simulation
# Wazuh Home Lab – SSH Brute Force Detection

## 📌 Overview
Project ini merupakan simulasi keamanan di Home Lab untuk menguji kemampuan **Wazuh (HIDS)** dalam mendeteksi aktivitas serangan, khususnya **SSH brute force attack**.

Simulasi dilakukan dari sisi attacker menggunakan Kali Linux, sementara target menggunakan Ubuntu Server dengan Wazuh Agent terpasang.

---

## 🧪 Attack Scenario
Serangan yang disimulasikan pada project ini:

- SSH brute force menggunakan **Nmap NSE (ssh-brute)**
- Target port: **22/tcp**
- Tujuan: mengamati perbedaan visibilitas log dan alert pada sisi host

---

## 🔍 Detection Result
Beberapa insight yang diperoleh:

- Aktivitas brute force **terdeteksi oleh Wazuh Agent**
- Alert muncul berdasarkan:
  - Multiple failed SSH login attempts
  - Authentication failure logs
- Deteksi bersifat **host-based**, bukan network-based

---

## 🛠️ Tools & Environment
**Attacker:**
- Kali Linux
- Nmap + NSE ssh-brute script

**Defender:**
- Ubuntu Server
- Wazuh Agent
- OpenSSH Server

---

## 📂 Repository Structure

wazuh-home-lab/
│── README.md
│── docs/
│── screenshots/
│── logs/


---

## 🎯 Learning Outcome
Melalui project ini saya belajar bahwa:
- Brute force attack memiliki jejak log yang jelas di sisi host
- Monitoring authentication log sangat penting untuk SOC Analyst
- Wazuh efektif untuk mendeteksi serangan berbasis credential abuse

---

## 🚀 Next Plan
- Menambahkan simulasi **network-based detection**
- Integrasi dengan **Suricata**
- Analisis perbedaan alert HIDS vs NIDS

---

## 📄 Documentation
- [Lab Topology](docs/lab-topology.md)
- [Attack Scenario](docs/attack-scenario.md)
- [Detection Analysis](docs/detection-analysis.md)


📢 Project ini dibuat sebagai bagian dari pembelajaran dan dokumentasi personal di bidang **Cybersecurity & SOC Analysis**.
>>>>>>> e4a42bc (initial Wazuh home lab: SSH brute force detection)
