# Detection Analysis – Wazuh SSH Brute Force Alert

## 📊 Overview
Setelah simulasi SSH brute force dijalankan,
Wazuh Agent berhasil mendeteksi aktivitas mencurigakan
berdasarkan log autentikasi pada server target.

Deteksi ini bersifat **host-based detection**,
di mana analisis dilakukan dari sisi endpoint, bukan traffic jaringan.

---

## 🧾 Log Source
Deteksi berasal dari log berikut:

- File log: `/var/log/auth.log`
- Service: OpenSSH
- Event utama:
  - Failed password
  - Authentication failure
  - Repeated login attempts

---

## 🚨 Alert Behavior

Selama simulasi berlangsung, Wazuh menghasilkan alert dengan karakteristik:
- Multiple alert dalam waktu singkat
- Source IP yang sama
- Target user berbeda (atau user yang sama berulang)

Alert muncul setelah ambang batas percobaan login gagal tercapai.

---

## 🧠 Detection Logic
Wazuh mendeteksi brute force berdasarkan:
- Pola login gagal berulang
- Frekuensi event yang tidak normal
- Korelasi antar event autentikasi

Ini menunjukkan bahwa Wazuh tidak hanya membaca satu log,
tetapi melakukan **event correlation**.

---

## 📈 Severity & Risk
Alert yang dihasilkan memiliki tingkat severity menengah hingga tinggi,
karena:
- Berpotensi menyebabkan credential compromise
- Menunjukkan reconnaissance aktif terhadap service SSH
- Umum digunakan sebagai tahap awal serangan lanjutan

---

## 🧩 Analysis Insight
Beberapa insight penting:
- Serangan tidak memerlukan exploit untuk terdeteksi
- Log autentikasi sudah cukup kuat sebagai indikator
- Monitoring SSH adalah kontrol keamanan dasar yang krusial

---

## 📌 Conclusion
Wazuh terbukti efektif dalam:
- Mendeteksi serangan berbasis kredensial
- Memberikan visibilitas aktivitas mencurigakan di host
- Membantu analyst memahami timeline serangan
