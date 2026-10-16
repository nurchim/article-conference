# Conference Lab — Jurnal vs Conference

Aplikasi edukasi interaktif Pertemuan 1 mata kuliah **Information Technology Conference (MTI26201)**, Magister Teknologi Informasi. Berdasarkan RPS dan dua artikel contoh yang diberikan dosen. Dapat di-host di GitHub dan **deploy ke Vercel tanpa backend**.

## Fitur

- **Beranda:** target belajar dan konteks.
- **Bandingkan:** 9 aspek beda jurnal vs conference, accordion interaktif.
- **Artikel Nyata:** perbandingan faktual dua artikel (metadata, metode, temuan, DOI).
- **Pilih Forum:** simulator pertimbangan venue dan checklist validasi.
- **Kuis:** 8 soal, feedback, nilai langsung.
- **Lembar Kerja:** tugas sesuai RPS, rubrik 40/40/20, ekspor jawaban ke TXT.
- **PDF Panduan:** tombol pada menu membuka `public/panduan-pertemuan-1.pdf`.

## Menjalankan secara lokal

Persyaratan: Node.js 20.19+ atau 22.12+ dan npm.

```bash
npm install
npm run dev
```

Buka URL yang tercetak di terminal (biasanya `http://localhost:5173`).

## Deploy GitHub → Vercel

1. Ekstrak ZIP ini. Buat repositori GitHub baru (misalnya `conference-learning-lab`).
2. Di folder proyek, jalankan:

   ```bash
   git init
   git add .
   git commit -m "Initial Conference Lab"
   git branch -M main
   git remote add origin https://github.com/USERNAME/conference-learning-lab.git
   git push -u origin main
   ```

3. Masuk ke Vercel → **Add New Project** → **Import Git Repository**.
4. Pilih repo tersebut. Vercel akan mengenali **Vite**. Build Command `npm run build`, Output Directory `dist`.
5. Klik **Deploy**. Setiap push baru ke `main` akan memicu deployment baru.

Alternatif deploy via Vercel CLI: `npx vercel` (ikuti instruksi login dan project setup).

## Sumber materi dan kehati-hatian

- RPS Information Technology Conference MTI26201 (28 September 2026), pertemuan 1.
- Sholikhin, A. T., dkk. (2026). *Dinamika dan Tingkat Pemulihan Kinerja Hotel Bintang di Pulau Jawa Sebelum, Saat, dan Setelah Pandemi COVID-19 Periode 2018–2025*. JIBEMA, 4(1), 2388–2405. https://doi.org/10.62421/jibema.v4i1.662
- Rif’ah, M. I., Wirjodirdjo, B., & Ciptomulyono, U. (2025). *Evaluating the Indonesian MSMEs’ Readiness in Implementing R-Framework for Promoting Circular Economy*. Management Science and Industrial Engineering, 520–527. IOS Press. https://doi.org/10.3233/ATDE250566
- IEEE Author Center, [Structure Your Paper](https://conferences.ieeeauthorcenter.ieee.org/write-your-paper/structure-your-paper/) dan [Submission Policies](https://conferences.ieeeauthorcenter.ieee.org/author-ethics/guidelines-and-policies/submission-policies/).

**Penting:** DOI tidak membuktikan pengindeksan Scopus. Status sumber dan tahun cakupannya harus diverifikasi pada indeks terkait. Aplikasi tidak mengklaim dua contoh memiliki status Scopus yang sama. Artikel contoh berasal dari bidang yang berbeda sehingga pembandingan difokuskan pada bentuk komunikasi ilmiah, bukan peringkat mutu atau hasil riset.

## Teknologi / privasi

Vite + JavaScript + CSS tanpa framework berat, responsif untuk mobile. Tidak menggunakan API key, database, autentikasi, analytics, ataupun pengiriman data pengguna. Hasil lembar kerja hanya diekspor lokal melalui browser.

## Pengembangan selanjutnya

Untuk mengganti konten, edit `src.js` (bagian `data`, `refs`, dan `questions`). Untuk mengubah tampilan, edit `style.css`.
