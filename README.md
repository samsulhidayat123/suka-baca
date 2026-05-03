# 📖 SUKA BACA Manga - Premium

SUKA BACA adalah platform baca manga dan manhwa berbasis web dengan antarmuka premium, cepat, dan responsif. Aplikasi ini dilengkapi dengan fitur autentikasi pengguna dan sistem komentar interaktif yang terintegrasi dengan **Supabase**.

## ✨ Fitur Utama

- **📱 Desain Responsif & Premium:** Tampilan elegan yang menyesuaikan dengan baik di perangkat desktop maupun mobile.
- **🌓 Mode Gelap & Terang:** Dilengkapi fitur *Theme Toggle* agar mata pengguna nyaman saat membaca.
- **🔍 Pencarian Cerdas:** Bar pencarian dinamis dengan animasi mulus untuk mencari judul komik favorit.
- **📂 Filter Kategori Otomatis:** Sistem filter (Semua, Manga, Manhwa, Buku) yang dinamis dan terhubung dengan database.
- **🔖 Riwayat Baca Terakhir:** Website akan mengingat *chapter* dan manga terakhir yang dibaca pengguna.
- **🔐 Sistem Autentikasi:** Fitur Login dan Register menggunakan **Supabase Auth**.
- **💬 Kolom Komentar:** Pengguna yang telah login dapat berdiskusi dan memberikan komentar di setiap *chapter*.
- **🚀 Performa Cepat:** Menggunakan *Lazy Loading* untuk memuat gambar *chapter* secara efisien.
- **📖 Navigasi Chapter Lanjutan:** Navigasi antar *chapter* melalui *dropdown*, tombol Prev/Next, maupun menggunakan *keyboard* (Arrow Left/Right).

## 🛠️ Teknologi yang Digunakan

- **Frontend:** HTML5, CSS3, Vanilla JavaScript.
- **Backend/Database:** [Supabase](https://supabase.com/) (PostgreSQL & Supabase Auth).
- **Lain-lain:** Supabase-js SDK V2.

## 🚀 Cara Menjalankan Proyek Secara Lokal

1. **Clone Repository**
   ```bash
   git clone https://github.com/username-kamu/nama-repo-kamu.git
   cd nama-repo-kamu/frontend
   ```

2. **Konfigurasi Supabase**
   Pastikan Anda sudah memiliki proyek di Supabase. Anda dapat mengatur variabel lingkungan (URL dan Key Supabase) pada file konfigurasi Anda (`config.js`) yang tertaut pada *file* `index.html`.
   
   *Contoh isi `config.js`:*
   ```javascript
   window.ENV = {
       SUPABASE_URL: 'https://proyek-kamu.supabase.co',
       SUPABASE_KEY: 'anon-key-kamu'
   };
   ```

3. **Jalankan Aplikasi**
   Karena proyek ini menggunakan HTML dan JS murni, Anda dapat menjalankannya dengan ekstensi seperti **Live Server** di VS Code, atau meng-*host* folder ini di server lokal manapun (seperti XAMPP/Node HTTP Server).
   
   *Catatan:* Sangat disarankan untuk membukanya melalui localhost/server lokal alih-alih klik ganda pada `index.html` (protokol `file://`) agar fitur *Auth* dan pengambilan data API Supabase berjalan lancar (mencegah isu CORS).

## 🗄️ Skema Database Supabase

Untuk menjalankan aplikasi ini, kamu memerlukan tabel berikut di Supabase kamu:
- **`manga_chapters`**: Berisi `judul`, `chapter`, `daftar_gambar` (JSON/Array), `kategori`, `created_at`.
- **`manga_comments`**: Berisi `judul`, `chapter`, `komentar`, `user_id`, `user_email`, `created_at`.

## 🤝 Dukungan

Jika Anda menyukai proyek ini, pertimbangkan untuk memberikan 🌟 **Star** di repository ini!

*Dibuat dengan ❤️ untuk para pembaca setia Manga dan Manhwa.*