# Analisis Logat Bicara Mahasiswa Universitas Pertamina Menggunakan MFCC

Proyek ini bertujuan untuk menganalisis logat bicara mahasiswa Universitas Pertamina dari berbagai daerah di Indonesia dengan menggunakan teknik _Mel-Frequency Cepstral Coefficients_ (MFCC). Dataset terdiri dari rekaman suara mahasiswa yang berasal dari lima daerah: Timur, Jawa, Medan, Sunda, dan Minang.

## 📌 Deskripsi Singkat

Mel-Frequency Cepstral Coefficients (MFCC) adalah metode ekstraksi fitur audio yang sering digunakan dalam pengenalan suara. Dalam proyek ini, MFCC digunakan untuk menangkap karakteristik akustik logat mahasiswa dari berbagai daerah, kemudian divisualisasikan dan disimpan untuk keperluan analisis dan pelatihan model machine learning ke depannya.

## 🎯 Tujuan Proyek

- Mengumpulkan data suara dari mahasiswa dengan logat khas daerah.
- Mengekstraksi ciri suara menggunakan MFCC.
- Menganalisis perbedaan logat berdasarkan fitur akustik.
- Menyediakan dasar data untuk pengembangan sistem pengenalan logat berbasis machine learning.

## 🗂️ Struktur Dataset

- Total 100 rekaman suara.
- 5 logat: Timur, Jawa, Medan, Sunda, Minang.
- Masing-masing logat diwakili oleh 2 partisipan (20 sampel per logat).
- Format audio: `.wav` (konversi otomatis dari format lain menggunakan `pydub` dan `ffmpeg`).

## 🧰 Tools & Library

- `Python 3.10+`
- [Librosa](https://librosa.org/): Ekstraksi fitur MFCC.
- `Pydub`: Konversi audio ke format `.wav`.
- `FFmpeg`: Backend konversi format audio.
- `Pickle`: Penyimpanan hasil ekstraksi MFCC.
- `NumPy`, `OS`: Pengelolaan file dan data numerik.

## 🔄 Alur Proses

1. **Konversi Audio**
   - Semua file audio dikonversi ke `.wav`.
   - Folder input dan output didefinisikan secara fleksibel.

2. **Ekstraksi MFCC**
   - MFCC diekstraksi dari setiap file `.wav`.
   - Hasil disimpan dalam format `.pkl`.

3. **Visualisasi**
   - Visualisasi MFCC per logat dilakukan untuk melihat pola spektral khas setiap aksen.

## 📊 Hasil Utama

- Setiap logat menghasilkan dimensi MFCC rata-rata yang berbeda.
- Contoh dimensi rata-rata:
  - Medan: `13 x 1227.5`
  - Jawa: `13 x 1200`
  - Sunda: `13 x 865.3`
- Visualisasi spektrogram MFCC menunjukkan perbedaan pola frekuensi dan distribusi energi.

## 🧠 Potensi Pengembangan

- Dataset ini dapat digunakan untuk:
  - **Pelatihan model klasifikasi logat** menggunakan machine learning.
  - **Klasifikasi aksen bahasa Indonesia** secara otomatis.
  - **Pengembangan sistem pengenalan suara yang lebih inklusif** terhadap aksen daerah.

## 💻 Cara Menjalankan

1. **Instalasi Dependensi**
    ```bash
    pip install librosa pydub numpy
    ```

2. **Pastikan FFmpeg terinstal**
    - [Download FFmpeg](https://ffmpeg.org/download.html) dan tambahkan ke PATH sistem.

3. **Jalankan Konversi Audio**
    ```bash
    python convert_to_wav.py
    ```

4. **Ekstraksi MFCC**
    ```bash
    python extract_mfcc.py
    ```

## 👨‍💻 Kontributor

- Alghifari Rasyid Zola — [alghifarirasyidzola@gmail.com](mailto:alghifarirasyidzola@gmail.com)  
- Bambang Istijab  
- Fauzan Azhima  

Mahasiswa Ilmu Komputer, Universitas Pertamina

## 📄 Lisensi

Proyek ini terbuka untuk penggunaan edukatif dan riset. Silakan fork dan modifikasi sesuai kebutuhan dengan menyertakan atribusi yang sesuai.
