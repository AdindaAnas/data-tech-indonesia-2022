# 📊 Decoding the Data & Tech Profession in Indonesia (2022)

> Analisis mendalam tentang lanskap karier Data & Teknologi di Indonesia berdasarkan **Kaggle ML & Data Science Survey 2022**

---

## 📌 Deskripsi Proyek

Proyek ini bertujuan mengungkap panorama pekerjaan di bidang **Data & Teknologi di Indonesia** pada tahun 2022. Dengan memfilter 111 responden profesional aktif dari Indonesia (dari total 23.997 responden global), analisis ini menjawab empat pertanyaan kunci seputar posisi pekerjaan, industri, gender, dan latar belakang pendidikan.

---

## ❓ Rumusan Masalah

| # | Pertanyaan |
|---|-----------|
| 1 | Apa saja **posisi pekerjaan teratas** di bidang Data & Tech di Indonesia? |
| 2 | **Industri mana** yang paling banyak merekrut profesional Data & Tech? |
| 3 | Bagaimana **distribusi gender** di bidang Data & Tech Indonesia? |
| 4 | Apa **latar belakang pendidikan** yang paling umum dimiliki profesional Data & Tech? |

---

## 🗂️ Dataset

| Atribut | Detail |
|---------|--------|
| **Sumber** | [Kaggle ML & Data Science Survey 2022](https://www.kaggle.com/competitions/kaggle-survey-2022) |
| **File** | `kaggle_survey_2022_responses.csv` |
| **Total Responden** | 23.997 |
| **Responden Indonesia (filtered)** | 111 |
| **Jumlah Kolom** | 296 |

### Kriteria Filter Data Indonesia

```python
df[
    (df["Q5"] == "No")                          # Bukan pelajar/mahasiswa
    & (df["Q24"].notnull())                     # Menjawab industri tempat bekerja
    & (df["Q23"] != "Currently not employed")   # Sedang aktif bekerja
    & (df["Q4"] == "Indonesia")                 # Berdomisili di Indonesia
]
```

---

## 🛠️ Tech Stack

| Kategori | Library |
|----------|---------|
| Data Manipulation | `pandas`, `numpy` |
| Visualisasi Interaktif | `plotly` (graph_objects, express, figure_factory) |
| Visualisasi Statis | `matplotlib` |
| Utility | `collections`, `jinja2` |

---

## 🚀 Cara Menjalankan

### 1. Clone / Download Proyek

```bash
git clone <repo-url>
cd datamining-indonesia-2022
```

### 2. Install Dependencies

```bash
pip install pandas numpy plotly matplotlib jinja2
```

Atau jalankan sel pertama di notebook — script otomatis menginstall semua library yang dibutuhkan.

### 3. Siapkan Dataset

Unduh dataset dari [Kaggle Survey 2022](https://www.kaggle.com/competitions/kaggle-survey-2022) dan letakkan file `kaggle_survey_2022_responses.csv` di direktori yang sama dengan notebook.

### 4. Jalankan Notebook

Buka dan jalankan seluruh sel notebook secara berurutan.

---

## 📊 Struktur Analisis

```
1. Install & Import Libraries
2. Load Dataset
3. Helper Functions (scatter plot, bar plot, funnel chart)
4. Filter Data Indonesia
5. Explorasi & Visualisasi
   ├── 5.1 Key Figures
   ├── 5.2 Rata-rata Pilihan Multiple-Choice
   ├── 5.3 Q1 — Top Job Positions
   ├── 5.4 Q2 — Industries & Work Activities
   │         ├── Scatter: Industry vs Role
   │         ├── Funnel: Core Activities of Data & ML Professionals
   │         └── Scatter: Task Distribution Across Roles
   ├── 5.5 Q3 — Gender Distribution
   └── 5.6 Q4 — Educational Qualifications
6. Kesimpulan
```

---

## 📈 Hasil & Temuan

### 1️⃣ Top Job Positions

**Data Scientist** dan **Data Analyst** merupakan dua posisi teratas yang paling banyak diisi profesional Data & Tech di Indonesia. Aktivitas kerja utama yang mendominasi meliputi:
- Analisis data untuk pengambilan keputusan bisnis
- Pembangunan dan pengelolaan infrastruktur data
- Eksperimen dan iterasi model machine learning

### 2️⃣ Industri Perekrut Terbesar

| Industri | Jumlah Responden |
|----------|-----------------|
| Academics / Education | 35 |
| Computers / Technology | 19 |
| Accounting / Finance | 11 |
| Manufacturing / Fabrication | 10 |
| Retail / Sales | 8 |
| Government / Public Service | 5 |
| Marketing / CRM | 5 |

Sektor **pendidikan** menjadi penyerap terbesar talenta Data & Tech di Indonesia, mengungguli sektor teknologi itu sendiri — menandakan tingginya kebutuhan akan pengajaran dan riset di bidang ini.

### 3️⃣ Distribusi Gender

Terdapat **kesenjangan gender yang signifikan**, dengan dominasi responden laki-laki. Kondisi ini mencerminkan perlunya upaya lebih besar dalam mendorong inklusivitas dan kesetaraan gender di bidang Data & Tech Indonesia.

### 4️⃣ Latar Belakang Pendidikan

Mayoritas profesional berpendidikan **Sarjana (S1)** sebagai minimum. Gelar **Magister (S2)** cukup umum terutama di posisi Research Scientist dan manajerial.

---

## 💡 Kesimpulan

Ekosistem Data & Tech di Indonesia pada 2022 menunjukkan pertumbuhan yang menjanjikan dengan permintaan tinggi lintas sektor, tidak hanya teknologi, tetapi juga pendidikan, keuangan, dan manufaktur. Namun, dua tantangan utama yang masih perlu diatasi adalah:

1. **Kesenjangan gender** — perempuan masih sangat underrepresented di industri ini.
2. **Kebutuhan talenta** — perluasan jalur pendidikan formal dan non-formal diperlukan untuk memenuhi permintaan yang terus tumbuh.

---

## 👤 Author

Proyek ini merupakan bagian dari analisis data mining menggunakan dataset publik Kaggle Survey 2022. Analisis ini bersifat eksploratif dan terbatas pada 111 responden profesional aktif dari Indonesia berdasarkan dataset Kaggle Survey 2022.

---

*Dataset: Kaggle ML & Data Science Survey 2022 | Filter: Profesional aktif di Indonesia (n=111)*
