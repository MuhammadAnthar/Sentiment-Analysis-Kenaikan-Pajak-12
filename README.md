# Sentiment Analysis: Kenaikan Pajak 12% (Twitter)

## 📘 Studi Kasus
Proyek ini menganalisis **sentimen publik di Twitter** terhadap isu **kenaikan pajak 12%**. Analisis mencakup distribusi sentimen, wordcloud untuk sentimen positif/negatif, analisis akun dengan interaksi tinggi, analisis mention & centrality dalam jaringan sosial, tren berdasarkan tanggal, serta evaluasi model klasifikasi sentimen menggunakan **SVM**.

## 🎯 Tujuan
1. Mengidentifikasi persebaran sentimen publik (positif, netral, negatif) terkait kenaikan pajak 12%.
2. Menggali kata-kata dominan pada sentimen positif dan negatif melalui **wordcloud**.
3. Menganalisis pola interaksi & jaringan (top user, mention terbanyak, centrality).
4. Membangun model klasifikasi sentimen menggunakan **SVM** dan mengevaluasi performanya.

## 📊 Data
Data berupa tweet terkait topik **kenaikan pajak 12%** yang telah dilabeli menjadi tiga kelas:
- **Negatif:** 1.841 tweet  
- **Netral:** 326 tweet  
- **Positif:** 43 tweet

> Distribusi menunjukkan mayoritas tweet bersentimen negatif (hal ini mengindikasikan respons publik cenderung tidak menyenangkan terhadap topik yang dianalisis).

## 🔎 Hasil dan Temuan

### 📌 Distribusi Sentimen
Mayoritas data adalah sentimen **negatif**, disusul **netral**, dan **positif** yang paling sedikit.

### ☁️ Wordcloud Sentimen Positif
Kata dominan pada sentimen positif antara lain **“pemerintah”**, serta kata terkait kebijakan dan ekonomi seperti **“ekonomi”**, **“kebijakan”**, dan **“penghasilan”**. Ini mengindikasikan sebagian kecil publik menilai isu/pembahasan ini dalam konteks kebijakan dan stabilitas ekonomi.

### ☁️ Wordcloud Sentimen Negatif
Sentimen negatif didominasi keluhan terkait **gaji, pendapatan, tarif, biaya hidup, kebijakan pemerintah**, termasuk isu **harga pokok, BPJS**, dan **pengangguran**.

### 👥 Pola Interaksi & Jaringan
- Akun personal tertentu memperoleh interaksi sangat tinggi (dua akun teratas >30.000 interaksi).
- Dari sisi “jumlah tweet terbanyak”, akun media seperti **kompascom** muncul dominan.
- Target mention terbanyak dipimpin **txtdrimedia** (92 mention), disusul **kumparan** (51) dan **kompascom** (31).
- Analisis centrality menunjukkan **txtdrimedia** sebagai node paling terhubung/berpengaruh, sementara **gue303030** berperan sebagai penghubung utama dalam jaringan.

### 📅 Tren Berdasarkan Tanggal
Terdapat puncak aktivitas signifikan pada **14/11/2024** sebanyak **440 data**, mengindikasikan lonjakan diskusi pada tanggal tertentu (kemungkinan dipicu peristiwa/kampanye).

## 🤖 Modeling (SVM)
Model **SVM** mencapai akurasi **80.81%**.  
Ringkasan performa:
- Kelas **positif** memiliki hasil paling baik (precision ~98%, recall ~93%, F1 ~95%).
- Kelas **negatif** precision tinggi tetapi recall rendah (model lebih sulit mengenali data negatif).
- Kelas **netral** recall tinggi tetapi precision rendah (masih terjadi kesalahan klasifikasi).

## ✅ Kesimpulan
Pembahasan kenaikan pajak 12% didominasi sentimen **negatif**, yang banyak berkaitan dengan isu ekonomi rumah tangga (gaji, biaya hidup, tarif, dan kebijakan). Walaupun demikian, ada sebagian kecil sentimen positif yang menyoroti aspek kebijakan dan stabilitas ekonomi. Model SVM memberikan performa yang cukup baik dengan akurasi ~80.81%, namun masih perlu perbaikan terutama untuk membedakan kelas negatif dan netral.
