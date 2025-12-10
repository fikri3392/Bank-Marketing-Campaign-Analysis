# Bank Marketing Campaign Analysis  
### Exploratory Data Analysis menggunakan Excel & PivotTable  
Dataset: [UCI Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing)  
45211 records │ 17 fitur │ Target: apakah nasabah subscribe term deposit (yes/no)

## Objective
Menemukan pola dan segmen nasabah yang paling potensial untuk kampanye telemarketing berikutnya hanya dengan Excel PivotTable & Chart (tanpa coding).

## 5 Insight & Metrik Paling Krusial

| # | Insight Utama                                                 | Conversion Rate / Nilai Kunci                  | Rekomendasi Bisnis                                      |
|---|----------------------------------------------------------------|------------------------------------------------|----------------------------------------------------------|
| 1 | Hasil kampanye sebelumnya (poutcome) adalah prediktor terkuat | **success → 64.7 %**<br>failure → 12.6 %<br>unknown → 9.2 % | Prioritaskan daftar nasabah dengan **poutcome = success** |
| 2 | Bulan kontak sangat memengaruhi konversi                      | Mar (52 %), Sep (46.5 %), Oct (43.8 %), Dec (46.7 %)<br>Mei hanya **6.7 %** | Hindari kampanye besar-besaran di bulan Mei             |
| 3 | Segmen pekerjaan tertentu jauh lebih responsif                | Student → 28.7 %<br>Retired → 22.8 %<br>Blue-collar hanya 7.3 % | Fokuskan calling ke **student & retired**                |
| 4 | Nasabah tanpa cicilan rumah (housing loan = no) 2× lebih mungkin subscribe | No housing loan → **16.7 %**<br>Yes housing loan → 7.7 % | Filter prospek yang **tidak sedang cicil KPR**          |
| 5 | Durasi panggilan adalah indikator sukses real-time           | Rata-rata **537 detik** (yes)<br>vs **221 detik** (no) | Agent harus berusaha memperpanjang call > 6 menit       |

![5 Key Charts](dashboard/bank_marketing_dashboard.pdf)  
*Semua chart dibuat hanya dengan PivotTable + Insert Chart di Microsoft Excel*

## File dalam Repository
- `/data/raw/bank-full.csv` → dataset lengkap (45.211 baris)  
- `/data/excel/Bank_Marketing.xlsx` → file Excel lengkap (7 sheet + 5 chart)  
- `Dashboard/` → gambar chart dalam file pdf

## Kesimpulan & Rekomendasi Kampanye Berikutnya
Dengan menerapkan 5 filter berikut secara bersamaan, bank dapat meningkatkan conversion rate dari 11.7 % menjadi > 50 %:
1. `poutcome = success`  
2. `month` ∈ {mar, sep, oct, dec}  
3. `job` ∈ {student, retired}  
4. `housing = no`  
5. Target durasi telepon minimal 8-10 menit

Analisis ini 100 % dilakukan di Excel tanpa satu baris kode pun.

Terima kasih!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](www.linkedin.com/in/fikri-miftahurrohman-14413b399)  
