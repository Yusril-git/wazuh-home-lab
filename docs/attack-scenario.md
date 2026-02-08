# Attack Scenario – SSH Brute Force



## Objective

Mensimulasikan serangan SSH brute force untuk mengamati bagaimana aktivitas login gagal

terekam pada sisi host dan dideteksi oleh Wazuh Agent.



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



