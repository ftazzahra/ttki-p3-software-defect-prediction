# Cost-Aware Software Defect Prediction Using Static Code Metrics and Machine Learning

Repositori eksperimen proyek akhir mata kuliah **Tata Tulis Karya Ilmiah (TTKI)**, Program Studi Sarjana Terapan Teknik Informatika, Politeknik Elektronika Negeri Surabaya (PENS).

## Anggota Kelompok
- **Zahrin Savana Khadijah** (`3124600063`) — Koordinator Literatur & Research Gap
- **Fatimah Azzahra** (`3124600068`) — Koordinator Eksperimen & Reproducibility

---

## Ringkasan Penelitian
- **Pertanyaan Penelitian (RQ):** Bagaimana pengaruh *class weighting* dan pemeringkatan modul berdasarkan probabilitas cacat terhadap persentase cacat yang ditemukan dalam batas anggaran inspeksi 20% total *Lines of Code* (LOC)?
- **Hipotesis Kerja:**
  - **H1:** Model berperingkat risiko menghasilkan prioritas inspeksi lebih baik daripada strategi acak.
  - **H2:** *Class weighting* meningkatkan *recall* kelas cacat dengan potensi penurunan *precision*.

---

## Sumber & Audit Dataset (Kaggle)
- **Nama Dataset:** NASA Software Defect Prediction (varian `JM1.arff`)
- **Tautan Sumber:** https://www.kaggle.com/datasets/aczy156/nasa-software-defect-prediction
- **Tanggal Unduh:** 25 November 2026
- **Lisensi:** CC0: Public Domain / NASA MDP Open Data
- **Karakteristik Data (`JM1.arff`):**
  - Jumlah observasi: 7.782 modul perangkat lunak (21 fitur metrik kode statis McCabe & Halstead + 1 kolom target `label`).
  - Distribusi kelas: 6.110 modul normal (`0` / `b'N'`, 78,51%) dan 1.672 modul cacat (`1` / `b'Y'`, 21,49%).
  - Kualitas data: 0 *missing values*, 0 nilai *infinity*, dan 0 duplikasi baris.
  - Kolom anggaran inspeksi: `LOC_TOTAL`.

---

## Struktur Repositori
```text
├── README.md                  # Dokumentasi utama proyek & instruksi reproduksi
├── requirements.txt           # Daftar pustaka utama Python
├── environment-freeze.txt     # Snapshot versi paket lengkap (pip freeze)
├── LICENSE                    # Lisensi MIT repositori
├── data/README.md             # Metadata, lisensi, dan tautan unduh dataset Kaggle
├── notebooks/                 # Jupyter Notebook berisi EDA, split, pemodelan, dan plot
├── results/metrics.csv        # Hasil evaluasi seluruh skenario eksperimen
├── figures/                   # Grafik Precision-Recall & Effort-Aware LOC Budget
├── references/                # Matriks sintesis 8 literatur ilmiah
└── paper/                     # Draf naskah artikel ilmiah IMRAD
