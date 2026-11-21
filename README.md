# Proyek Riset Laboratorium: Age-Standardized Rate (ASR) Insiden dan Kematian Kanker beserta Konsumsi dan Indeks Ekonomi Berbagai Negara

Repositori ini berisi data ASR insiden kanker dan kematian yang disebabkannya, Indeks sosial ekonomi, dan pola konsumsi dari 113 negara beserta analisisnya. Spesifik pada repositori ini, analisis hanya dilakukan pada ASR kanker serviks terhadap indeks sosial ekonomoi dan pola konsumsi menggunakan PCA dan ANOVA. Repositori ini dibuat sebagai tugas akhir proyek riset laboratorium (PRL) di Departemen Fisika UI pada tahun 2024.

## Data
Data dikumpulkan secara manual dari sumber publik (lihat DATA_SOURCES.md). Tahun data berkisar 2019 sampai 2023. File: data/PRL_2024.xlsx.

## Metode
ASR dikelompokkan menurut kuartil (empat kelompok) dan median (dua kelompok), fitur distandardisasi, lalu dianalisis dengan PCA dan ANOVA (f_classif, scikit-learn).

## Cara menjalankan (PowerShell)
```
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
jupyter notebook notebooks/PCA_Cervix_Cancer_Inc.ipynb
```

## Hasil


## Keterbatasan
- Analisis antarnegara pada satu potret waktu; tahun data berbeda-beda.
- Menunjukkan korelasi antarkelompok, bukan hubungan sebab-akibat.
- Belum ada model prediktif atau validasi.

## Kontributor Data
- Devin Syarazan, S.Si.
- Khalishia Fira Haninda, S.Si.
- Vira Rahmawati, S.Si.
- Muhammad Dafi Rayhan Haryadi, S.Si.
- Muhammad Aliza Mudrikah, S.Si.

## Lisensi dan sitasi
