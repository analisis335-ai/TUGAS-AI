# Pengenal Jumlah Jari – Teachable Machine

Website klasifikasi gambar yang memakai model buatan kelompok kami di Teachable Machine.
Model mengenali dua kelas: **3 jari** dan **5 jari**. Prediksi bisa dilakukan lewat
kamera (real-time) atau dengan mengunggah gambar.

## Teknologi

- HTML, CSS, dan JavaScript
- [TensorFlow.js](https://www.tensorflow.org/js)
- [Teachable Machine Image](https://github.com/googlecreativelab/teachablemachine-community) (library `@teachablemachine/image`)

## Struktur proyek

```
index.html      -> halaman web
model.json      -> arsitektur model
metadata.json   -> daftar kelas
weights.bin     -> bobot model
README.md       -> dokumentasi
```

Semua file berada dalam satu folder yang sama. Model dimuat otomatis dari file-file tersebut
saat halaman dibuka.

## Cara menggunakan

1. Buka halaman web, tunggu tulisan **"Model siap"** muncul.
2. Pilih salah satu:
   - **Kamera**: klik *Nyalakan kamera*, izinkan akses kamera, lalu tunjukkan jari ke kamera.
   - **Unggah gambar**: klik *Pilih gambar* lalu pilih foto.
3. Hasil prediksi tampil berupa kelas teratas dan persentase untuk setiap kelas.

## Menjalankan di komputer

Halaman harus dibuka lewat server, tidak bisa dengan klik dua kali pada `index.html`
(browser memblokir pembacaan `model.json` dari file lokal).

Pilih salah satu:

- **VS Code**: install ekstensi *Live Server*, klik kanan `index.html`, lalu pilih *Open with Live Server*.
- **Python**: jalankan perintah berikut di folder proyek, lalu buka `http://localhost:8000`.

  ```
  python -m http.server 8000
  ```

## Menayangkan lewat GitHub Pages

1. Unggah semua file di atas ke repository GitHub (langsung di halaman utama repository, bukan di dalam subfolder).
2. Buka **Settings** → **Pages**.
3. Pada *Branch* pilih `main` dan folder `/ (root)`, lalu klik **Save**.
4. Tunggu 1–2 menit, lalu buka link yang muncul, bentuknya `https://username.github.io/nama-repo/`.

## Catatan

- Halaman membutuhkan koneksi internet untuk memuat library TensorFlow.js dan Teachable Machine.
- Akses kamera hanya bekerja di `localhost` atau alamat `https`.
