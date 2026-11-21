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
  Ringkasan temuan (detail lengkap: [Laporan PRL](results/Laporan%20PRL_Muhammad%20Aliza%20Mudrikah.pdf)):

  - **Pengelompokan:** Pembagian dua kelompok (median) memisahkan negara ASR rendah dan tinggi lebih baik daripada empat kelompok
  (kuartil), baik pada plot PCA maupun nilai F ANOVA.
  - **PCA:** PC1 didominasi fertility rate, GDP per kapita, dan konsumsi babi. Plot 2D masih tumpang-tindih, plot 3D (PC1–PC3) lebih terpisah.
  - **ANOVA (α = 0,05, dua kelompok):** Semua fitur signifikan kecuali konsumsi domba/kambing.

  | Fitur | F-value | p-value |
  |---|---|---|
  | Fertility rate | 45,46 | 7,3e-10 |
  | GDP per kapita | 40,87 | 4,0e-09 |
  | Babi | 28,96 | 4,2e-07 |
  | Garam | 26,13 | 1,3e-06 |

  - **Kesimpulan:** Fertility rate, GDP per kapita, dan pola konsumsi berasosiasi secara statistik dengan tingkat ASR insiden kanker serviks antarnegara.


## Kontributor Data dan Analisis
- Devin Syarazan, S.Si.
- Khalishia Fira Haninda, S.Si.
- Vira Rahmawati, S.Si.
- Muhammad Dafi Rayhan Haryadi, S.Si.
- Muhammad Aliza Mudrikah, S.Si.
- Syahril Siregar, Ph.D. (Supervisor)

## Sitasi
Jika hendak menggunakan proyek ini, silakan sitasi:
```bibtex
@article{aliza204prl,
  title     = {ANALISIS AGE-STANDARDIZED RATE INSIDEN
KANKER SERVIKS BERDASARKAN FERTILITY RATE,
GDP, DAN POLA KONSUMSI DI BERBAGAI NEGARA
DENGAN METODE STATISTIKA MULTIVARIAT},
  author    = {Muhammad Aliza Mudrikah},
  year      = {2024},
  school    = {Universitas Indonesia},
  type      = {Article}
}
```

## License
Proyek ini dibagikan sebagai referensi akademik. Silakan kontak penulis untuk penggunaan ulang.
