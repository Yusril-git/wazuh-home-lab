\# SSH Brute Force Attack Scenario



\## Objective

Mensimulasikan serangan SSH brute force untuk menguji kemampuan Wazuh Agent dalam mendeteksi percobaan login berulang.



\## Attacker

\- Kali Linux

\- Nmap NSE: ssh-brute



\## Target

\- Ubuntu Server

\- OpenSSH

\- Wazuh Agent



\## Steps

1\. Scanning port 22

2\. Eksekusi brute force

3\. Generasi failed authentication logs



\## Expected Result

\- Multiple authentication failure logs

\- Wazuh alert triggered



