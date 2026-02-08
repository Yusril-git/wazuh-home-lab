\# Lab Topology



\## Overview

Home lab ini dibuat untuk mensimulasikan skenario serangan dan deteksi keamanan berbasis host

menggunakan Wazuh sebagai HIDS (Host-based Intrusion Detection System).



Lab terdiri dari satu attacker machine dan satu target server yang dimonitor oleh Wazuh Agent.



\## Topology Diagram (Logical)



Attacker (Kali Linux)

&nbsp;       |

&nbsp;       |  SSH Brute Force

&nbsp;       |

Target (Ubuntu Server)

&nbsp;       |

&nbsp;       |  Log Monitoring

&nbsp;       |

Wazuh Agent → Wazuh Manager



\## Environment Detail



\### Attacker Machine

\- OS: Kali Linux

\- Role: Offensive simulation

\- Tools:

&nbsp; - Nmap

&nbsp; - NSE script: ssh-brute



\### Target Machine

\- OS: Ubuntu Server

\- Services:

&nbsp; - OpenSSH (port 22)

\- Security Agent:

&nbsp; - Wazuh Agent



\### Detection Platform

\- Wazuh Manager

\- Function:

&nbsp; - Log analysis

&nbsp; - Alert generation

&nbsp; - Rule-based detection



\## Network Type

\- Internal / Home Lab Network

\- No exposure to public internet



