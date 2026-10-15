# 📘 GuruPintar AI — Offline AI Study Assistant

> **Asisten Pembelajaran Cerdas Berbasis Modul — 100% Berjalan Offline Tanpa Koneksi Internet.**

GuruPintar AI adalah aplikasi web edukasi interaktif yang dirancang khusus untuk mendampingi siswa dan mahasiswa belajar secara mendalam, mandiri, dan terarah. Aplikasi ini memproses modul pembelajaran sepenuhnya di sisi peramban (client-side) tanpa memerlukan server eksternal, kunci API berbayar, maupun koneksi internet aktif.

---

## ✨ Fitur Unggulan

- **🔒 Proteksi Materi Modul (Teks Tersembunyi)**  
  Teks modul mentah tidak ditampilkan secara langsung pada ruang belajar/chat. Hal ini menjaga integritas proses belajar agar pengguna tidak sekadar membaca contekan, melainkan aktif bertanya, menganalisis konsep, dan menguji daya ingat bersama asisten AI.
- **⚡ 100% Offline Ready (Zero Dependency)**  
  Dapat langsung dibuka cukup dengan mengklik dua kali berkas `index.html` di komputer atau laptop mana pun (protokol `file:///`). Dilengkapi Service Worker dan Web App Manifest untuk dukungan PWA (Progressive Web App).
- **📚 10 Preset Modul Pembelajaran Terintegrasi**  
  Telah dilengkapi koleksi modul siap pakai lintas disiplin ilmu:
  1. *Sejarah*: Peristiwa Rengasdengklok & Proklamasi Kemerdekaan Indonesia
  2. *Biologi*: Sistem Pencernaan dan Metabolisme pada Manusia
  3. *Fisika*: Mekanika Klasik dan Hukum-Hukum Gerak Newton
  4. *Kimia*: Termokimia, Perubahan Entalpi, dan Laju Reaksi
  5. *Matematika*: Kalkulus Diferensial dan Aplikasi Integral
  6. *Sosiologi*: Struktur Sosial, Stratifikasi, dan Diferensiasi
  7. *Geografi*: Dinamika Litosfer, Tektonisme, dan Mitigasi Bencana
  8. *Ekonomi*: Sistem Moneter, Lembaga Keuangan, dan Pasar Modal
  9. *Informatika*: Arsitektur Von Neumann, Model OSI, dan Keamanan Jaringan
  10. *Bahasa Indonesia*: Sistematika Karya Tulis Ilmiah (KTI) & Kajian Sastra
- **➕ Tambah Modul Belajar Sendiri (Custom Module)**  
  Pengguna dapat menambahkan modul pelajaran sendiri dengan mengunggah berkas teks (`.txt`, `.md`, `.json`) melalui fitur *drag-and-drop* atau menempelkan (*paste*) catatan silabus ke formulir. Modul disimpan secara aman di `localStorage` peramban.
- **🎯 Mode Kuis & Evaluasi Interaktif**  
  AI mampu membuat pertanyaan pilihan ganda (A, B, C, D) secara otomatis dari materi modul aktif. Dilengkapi umpan balik koreksi instan, penjelasan konsep, dan sistem skor (*point reward*).
- **🔊 Sintesis Suara (Audio Text-to-Speech)**  
  Dapat membacakan penjelasan materi secara lisan menggunakan Web Speech API bawaan peramban secara offline.
- **🌓 Tema Gelap & Terang Modern**  
  Desain antarmuka *glassmorphism* modern dengan transisi halus, palet warna elegan, dan tipografi nyaman untuk sesi belajar panjang.

---

## 🚀 Cara Menjalankan Aplikasi

### Opsi 1: Langsung Offline (Tanpa Instalasi Apapun)
1. Unduh (*clone* atau *download ZIP*) repositori ini ke komputermu.
2. Buka folder proyek dan klik ganda pada berkas **`index.html`**.
3. Aplikasi akan langsung terbuka di browser favoritmu (Google Chrome, Microsoft Edge, Firefox, Safari, dll.) dan siap digunakan!

### Opsi 2: Menghosting Gratis di GitHub Pages
Repositori ini telah disiapkan agar siap di-hosting langsung di GitHub Pages:
1. Unggah kode ke repositori GitHub pribadimu (`git push origin main`).
2. Masuk ke tab **Settings** di repositori GitHub.
3. Di panel sebelah kiri, pilih menu **Pages**.
4. Pada bagian **Build and deployment > Branch**, pilih branch `main` dan folder `/(root)`, lalu klik **Save**.
5. Situs web interaktifmu akan langsung aktif pada tautan `https://<username>.github.io/<nama-repo>/`.

---

## 📁 Struktur Direktori

```
AI-Study-Assistant/
├── index.html              # Antarmuka web utama
├── manifest.json           # Konfigurasi PWA (Web App Manifest)
├── sw.js                   # Service Worker untuk caching aset offline
├── .gitignore              # Konfigurasi pengabaian file Git
├── README.md               # Dokumentasi lengkap proyek
├── css/
│   └── style.css           # Desain sistem responsif, tema gelap/terang, dan micro-animations
├── js/
│   ├── presets.js          # Basis data 10 modul preset bawaan kurikulum
│   ├── ai-engine.js        # Mesin NLP pedagogis, ekstraksi semantik, dan generator kuis offline
│   └── app.js              # Pengendali UI, event handler, audio TTS, dan penyimpanan lokal
├── assets/
│   ├── icon.svg            # Ikon logo vektor beresolusi tinggi
│   └── bot-avatar.svg      # Avatar visual GuruPintar AI
├── Koleksi_Modul/          # Arsip berkas teks silabus modul pembelajaran (.txt)
└── Koleksi_Modul_PDF/      # Dokumen modul referensi kurikulum (.pdf)
```

---

## 💡 Panduan Berinteraksi dengan GuruPintar AI

Kamu dapat mengetik berbagai jenis instruksi belajar di kotak pesan, antara lain:
- **Tanya Konsep Kunci**: *"Apa perbedaan reaksi eksoterm dan endoterm?"* atau *"Jelaskan fungsi enzim pepsin di lambung!"*
- **Rumus & Perhitungan**: *"Bagaimana rumus Hukum II Newton dan beri contoh perhitungannya?"*
- **Minta Rangkuman**: *"Rangkum seluruh poin penting materi modul ini!"*
- **Uji Pemahaman**: *"Uji saya dengan kuis!"* atau cukup klik tombol **🎯 Kuis Cepat** di navigasi atas.
- **Contoh Kasus Nyata**: *"Beri contoh nyata penerapan inersia dalam kehidupan sehari-hari."*

---

## 🛠️ Teknologi yang Digunakan

- **HTML5**: Struktur semantik dengan dukungan aksesibilitas penuh.
- **CSS3 (Vanilla)**: Desain kustom, CSS variables, Glassmorphism, CSS Grid & Flexbox, serta responsif di desktop maupun gawai seluler.
- **JavaScript (ES6+)**: Mesin pencarian semantik (TF-IDF), pengenalan intensi (Intent Classification), manipulasi DOM reaktif, dan Web Speech API.
- **Web Storage API**: Penyimpanan modul kustom dan skor progres belajar secara lokal di peramban (`localStorage`).

---

## 📄 Lisensi

Proyek ini dirilis di bawah lisensi terbuka [MIT License](LICENSE). Bebas digunakan, dipelajari, dan dikembangkan untuk keperluan pendidikan.