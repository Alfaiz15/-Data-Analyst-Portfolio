# ✈️ Root Cause Analysis Keterlambatan Penerbangan: End-to-End Data Workflow (Excel - Tableau)

## 📌 Ringkasan Eksekutif (Executive Summary)

Proyek ini adalah studi kasus **Operational Performance** yang berfokus pada **Root Cause Analysis (RCA)** keterlambatan penerbangan. Saya menerapkan *end-to-end data workflow*, mulai dari *Data Cleansing* di **Excel/Google Sheets** hingga visualisasi profesional di **Tableau**, untuk menghasilkan *actionable insights* bagi tim Operasional dalam meningkatkan kinerja ketepatan waktu (*On-Time Performance*).

## 🛠️ Tools dan Data

* **Data Engineering & Cleansing:** Microsoft Excel / Google Sheets
* **Visualisasi & Dashboarding:** Tableau Desktop
* **Data Source:** Data penyebab keterlambatan penerbangan (`Airline_Delay_Cause.csv`).

---

## ⚙️ Workflow Data Analyst

### Fase 1: Data Cleansing & Feature Engineering (Excel/Sheets)

Fase ini esensial untuk menyiapkan data agar metrik operasional dapat dihitung dengan akurat.

| Tugas | Tujuan Operasional | Metrik Kunci yang Dihasilkan |
| :--- | :--- | :--- |
| **Data Cleaning** | Memastikan *data integrity* pada nama maskapai dan bandara. | Konsistensi data melalui fungsi `TRIM()` dan `Remove Duplicates`. |
| **Total Waktu Delay** | Menghitung KPI utama kinerja operasional. | Total waktu tunda (menit) dari semua penyebab per entitas. |
| **Kontribusi Penyebab** | Mengukur *share* setiap faktor dalam total *delay* (misal: *Carrier Delay*). | Persentase kontribusi per penyebab. |
| **Klasifikasi Risiko** | *Flagging* bandara/maskapai berisiko tinggi. | Kategori risiko operasional (`High Risk`, `Normal`). |

### Fase 2: Analisis Kunci dan Visualisasi (Pivot Table & Tableau)

Wawasan diolah di Excel dan dikomunikasikan secara visual melalui Tableau.

| Analisis/Visualisasi | Fokus Operasional | Wawasan Utama |
| :--- | :--- | :--- |
| **Pivot Table** | Menentukan *Root Cause* dan *Bottleneck* teratas. | Identifikasi **Top 10 Bandara** dan **Maskapai** dengan *delay* tertinggi. |
| **Peta Hotspot** | Visualisasi Geografis (Tableau). | Menunjukkan lokasi **Hotspot Operasional** untuk intervensi yang tepat sasaran. |
| **Kontribusi Delay** | Stacked Bar Chart (Tableau). | Membandingkan persentase masalah **Internal** (*Carrier Delay*) vs **Eksternal** (*Weather/NAS Delay*). |
| **Tren Waktu** | Line Chart (Tableau). | Memantau perubahan kinerja bulanan dan dampak musiman (*Seasonal Trends*). |

---

## 💡 Key Insights & Rekomendasi Strategis

Analisis ini memberikan dasar bagi keputusan **Operations** yang terukur:

1.  **Isu Internal:** Jika **Carrier Delay** dominan, fokus perbaikan dialihkan ke **Manajemen Kru** dan jadwal *maintenance*.
2.  **Mitigasi Risiko:** Data *Weather Delay* digunakan untuk merekomendasikan penambahan **Buffer Time** pada rute yang rentan risiko cuaca.
3.  **Targeted Improvement:** Daftar Bandara *Top 10 Delay* menjadi target prioritas untuk *review* alur kerja dan koordinasi *Air Traffic Control* (mengurangi **NAS Delay**).
