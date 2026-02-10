# Lab Topology

## 🎯 Objective
Membangun Home Lab untuk mensimulasikan dan menganalisis deteksi serangan
SSH brute force menggunakan Wazuh (Host-based IDS).

## 🧱 Environment

<<<<<<< HEAD
### Attacker
- OS: Kali Linux
- Tool: Nmap (NSE ssh-brute)

### Target
- OS: Ubuntu Server
- Service: OpenSSH
- Security Agent: Wazuh Agent
=======
\## 🎯 Objective

Membangun Home Lab untuk mensimulasikan dan menganalisis deteksi serangan

SSH brute force menggunakan Wazuh (Host-based IDS).



\## 🧱 Environment



\### Attacker

\- OS: Kali Linux

\- Tool: Nmap (NSE ssh-brute)



\### Target

\- OS: Ubuntu Server

\- Service: OpenSSH

\- Security Agent: Wazuh Agent



\### Monitoring

\- Wazuh Manager + Dashboard



\## 🌐 Network Topology

\- Attacker dan Target berada dalam satu jaringan internal (NAT / Host-only)

\- Serangan dilakukan langsung ke port 22/tcp



\## 🧩 Notes

Topologi ini merepresentasikan skenario dasar yang umum

ditemukan pada lingkungan internal server.
>>>>>>> 70bc9f7 (add detection analysis for SSH brute force using Wazuh)

### Monitoring
- Wazuh Manager + Dashboard

## 🌐 Network Topology
- Attacker dan Target berada dalam satu jaringan internal (NAT / Host-only)
- Serangan dilakukan langsung ke port 22/tcp

## 🧩 Notes
Topologi ini merepresentasikan skenario dasar yang umum
ditemukan pada lingkungan internal server.
