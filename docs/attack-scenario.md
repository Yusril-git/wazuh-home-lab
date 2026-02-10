<<<<<<< HEAD
# Attack Scenario – SSH Brute Force



## Objective
=======
\# Attack Scenario – SSH Brute Force Simulation



\## 🕒 Background
>>>>>>> 70bc9f7 (add detection analysis for SSH brute force using Wazuh)

Pada lab ini, saya melakukan simulasi serangan SSH brute force

untuk memahami bagaimana aktivitas brute force tercatat di sisi host

dan bagaimana Wazuh mendeteksinya.



<<<<<<< HEAD
## Attack Type

- Credential-based attack

- SSH brute force



## Tools Used

- Nmap

- NSE Script: ssh-brute



## Attack Flow



1. Attacker melakukan scanning terhadap target

2. Ditemukan port 22 (SSH) dalam kondisi open

3. Attacker menjalankan brute force menggunakan wordlist

4. Target menghasilkan multiple failed login attempts

5. Log authentication tercatat pada sistem



## Indicators Generated

- Repeated failed SSH login attempts

- Invalid user authentication

- Authentication failure logs



## Purpose of Simulation

- Melatih pemahaman log-based detection

- Memahami pola serangan brute force

- Melihat keterbatasan host-based detection
=======
Simulasi ini meniru skenario umum di mana server Linux

menjadi target percobaan login berulang oleh attacker.



---



\## 🎯 Attack Objective

\- Menguji apakah aktivitas brute force SSH dapat:

&nbsp; - Tercatat di authentication log

&nbsp; - Dideteksi oleh Wazuh Agent

&nbsp; - Menghasilkan alert di Wazuh Dashboard



---



\## ⚔️ Attack Method



\### Tool yang digunakan

\- Nmap dengan NSE script `ssh-brute`

\- Port target: `22/tcp`



\### Command Execution

Serangan dijalankan dari mesin attacker (Kali Linux) dengan tujuan

melakukan percobaan login SSH berulang menggunakan kombinasi kredensial.



Aktivitas ini menghasilkan:

\- Multiple failed login attempts

\- Repeated authentication failure



---



\## 🧾 Observed Behavior on Target

Selama simulasi berlangsung, server target mencatat:

\- Log `Failed password` pada `/var/log/auth.log`

\- Percobaan login berulang dari satu IP attacker

\- Interval login yang relatif cepat (indikasi brute force)



---



\## 📌 Key Point

Meskipun serangan dilakukan melalui jaringan,

indikator utama serangan terlihat jelas di sisi host,

bukan dari traffic network secara langsung.
>>>>>>> 70bc9f7 (add detection analysis for SSH brute force using Wazuh)



