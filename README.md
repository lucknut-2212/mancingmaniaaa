🎣 Mancing Maniaaa - Leaderboard Edition

Mancing Maniaaa adalah game memancing interaktif berbasis web (HTML5 Canvas) yang sangat dioptimalkan untuk perangkat mobile. Pada versi Leaderboard Edition ini, game berubah menjadi mode Survival/Time Attack yang mendebarkan! Kumpulkan skor, penuhi target dalam 90 detik untuk naik level, dan ukir namamu di papan peringkat global!

✨ Fitur Utama

⏱️ Mode Survival 90 Detik: Kamu hanya punya 90 detik per level. Capai target skor (kelipatan 300) untuk mereset waktu dan naik ke level berikutnya! Jika gagal, Game Over.

🏆 Global Leaderboard (Google Sheets): Skor akhir dan waktu bertahanmu akan otomatis dikirim ke Google Sheets menggunakan Google Apps Script (GAS) saat Game Over.

👤 Karakter Vector HD & Visual Perahu Dinamis: Karakter utama di-render tajam menggunakan teknik Vector Canvas. Setiap barang yang kamu beli di Toko (Boks Es, Pancingan, Sonar, Lampu Petromaks, Minuman Energi) akan langsung muncul di atas kapalmu!

🛠️ Sistem Aksesoris (Buff Pasif): * 📡 Sonar Portabel: Mengurangi lonjakan tarikan ikan liar hingga 50%.

🏮 Lampu Petromaks: Meningkatkan kemungkinan munculnya ikan langka/monster di malam hari.

⚡ Minuman Energi: Menguras stamina ikan 2x lebih cepat saat ditarik di Sweet Spot.

🐟 Jurnal Ikan & Boks Es Dinamis: Gambar ikan di UI bukan lagi lingkaran warna biasa, melainkan ikon vektor yang dibentuk sesuai wujud asli ikan yang kamu tangkap.

🌊 Lingkungan Sesuai Bioma & Bioluminescence: Latar belakang pulau, karang, bangkai kapal, atau palung laut akan berubah sesuai lokasimu. Di malam hari pada laut dalam, plankton dan ikan akan memancarkan cahaya neon (bioluminescence).

📳 Haptic Feedback & Swipe-to-Counter: Efek getaran di mobile saat melempar kail atau digigit ikan. Melawan monster laut? Usap (swipe) layarmu ke arah yang berlawanan saat mereka mencoba kabur!

🚀 Cara Bermain

Masukkan Nama: Masukkan namamu di layar awal untuk dicatat di Leaderboard.

Lempar Kail (Power Meter): Ketuk tombol LEMPAR untuk memulai pengukur kekuatan. Ketuk lagi saat bar penuh untuk melempar kail sedalam mungkin.

Tarik (Reel): Tahan tombol TARIK saat ikan memakan umpan. Jaga indikator di bar biru (Sweet Spot) untuk menguras stamina ikan.

Jaga Tarikan: Jangan biarkan bar merah penuh (hingga muncul tanda !), atau tali akan putus! Lepas tombol untuk mengendurkan tali.

Perhatikan Arah: Jika muncul peringatan "SWIPE KE KANAN/KIRI", segera usap layar ke arah tersebut untuk menggagalkan perlawanan ikan monster.

Beli Upgrade: Masuk ke Toko untuk menjual ikan dan meng-upgrade peralatan agar kamu bisa mencapai skor lebih tinggi sebelum waktu 90 detik habis!

🛠️ Instalasi & Integrasi Leaderboard

Game ini murni menggunakan satu file HTML (Single-File Application). Anda bisa langsung membukanya di browser.

Setup Google Sheets untuk Papan Skor (Leaderboard):

Untuk mengaktifkan fitur penyimpanan skor otomatis, ikuti langkah ini:

Buat Google Sheets baru (misalnya "Leaderboard Mancing Mania").

Buka menu Ekstensi > Apps Script.

Copy-paste kode berikut ke dalam editor skrip:

function doPost(e) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  var nama = e.parameter.Nama || "Tanpa Nama";
  var score = e.parameter.Score || 0;
  var minutes = e.parameter.Minutes || 0;
  sheet.appendRow([nama, score, minutes]);
  return ContentService.createTextOutput("Success").setMimeType(ContentService.MimeType.TEXT);
}


Klik Terapkan (Deploy) > Deployment baru (New deployment).

Pilih tipe Aplikasi Web (Web App).

Set Jalankan sebagai menjadi Saya (Me), dan Yang memiliki akses menjadi Siapa saja (Anyone).

Selesaikan otorisasi dan salin URL Web App yang diberikan.

Buka file Index.html game ini, cari baris const GAS_URL = "URL_GOOGLE_APPS_SCRIPT_ANDA_DISINI"; dan ganti dengan URL Web App milik Anda.

(Catatan: Untuk pengalaman bermain terbaik, mainkan melalui perangkat mobile sungguhan atau gunakan fitur Device Simulation di browser desktop).

☕ Dukung Kreator

Suka dengan game ini? Dukung terus pengembangan game buatan lokal dengan membelikan kreator kopi melalui Saweria!

📜 Lisensi & Kredit

Game ini dikembangkan menggunakan Canvas API bawaan HTML5 dan menggunakan Phosphor Icons untuk antarmuka pengguna.

Created with ❤️ by Lucknut Gaming
