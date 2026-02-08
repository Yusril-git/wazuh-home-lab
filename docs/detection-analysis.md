\# Detection Analysis – Wazuh HIDS



\## Detection Method

Deteksi dilakukan secara host-based melalui analisis log sistem,

bukan melalui inspeksi traffic jaringan.



\## Log Source

\- `/var/log/auth.log`

\- SSH authentication logs



\## Detection Behavior

Wazuh Agent mendeteksi:

\- Multiple failed SSH login attempts

\- Authentication failure patterns

\- Repeated login attempts from the same source



\## Alert Characteristics

\- Alert severity: medium

\- Triggered by rule-based detection

\- Fokus pada authentication abuse



\## Analysis Result

\- Serangan berhasil terdeteksi di sisi host

\- Tidak diperlukan visibility network traffic

\- Efektif untuk mendeteksi brute force berbasis credential



\## Limitation

\- Tidak menampilkan detail payload jaringan

\- Tidak mendeteksi scanning sebelum login attempt



\## Conclusion

Wazuh efektif sebagai HIDS untuk mendeteksi serangan brute force SSH,

namun akan lebih optimal jika dikombinasikan dengan NIDS seperti Suricata.



