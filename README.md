# ♥ BORIMMM SHARE ♥

Shared list app — untuk Borimmm & pacar. Bisa dipasang di home screen iPhone.

## ⚙️ Cara Setup Firebase (5 menit)

### 1. Buat Firebase Project
1. Buka https://console.firebase.google.com/
2. Klik **Create a project** (Buat project)
3. Nama project: `borimmm-share`
4. Klik Create, ikuti step, sampe masuk dashboard

### 2. Register Web App
1. Di dashboard Firebase, klik **Settings** (⚙️) > **Project settings**
2. Scroll ke **Your apps** > klik **Add app** > **Web** (icon `</>`)
3. Kasih nama: `Borimmm Share`
4. Klik **Register app**
5. Akan muncul kode seperti ini:
   ```js
   const firebaseConfig = {
     apiKey: "AIzaSy...",
     authDomain: "borimmm-share.firebaseapp.com",
     databaseURL: "https://borimmm-share-default-rtdb.firebaseio.com",
     projectId: "borimmm-share",
     storageBucket: "borimmm-share.firebasestorage.app",
     messagingSenderId: "123456789",
     appId: "1:123456789:web:abc123"
   };
   ```
6. **Copy semua isi `firebaseConfig`** (dari `{` sampai `}`) — simpan sementara

### 3. Enable Anonymous Auth
1. Di sidebar kiri, klik **Authentication** > **Sign-in method**
2. Klik **Add new provider** > **Anonymous** (atau langsung cari)
3. **Enable** Anonymous sign-in
4. Klik Save

### 4. Enable Realtime Database
1. Di sidebar kiri, klik **Build** > **Realtime Database**
2. Klik **Create Database**
3. Pilih region (pilih yang terdekat, misal `asia-southeast1`)
4. Pilih mode **Start in test mode** (aman untuk test)
5. Klik Enable

### 5. Isi Config ke File
1. Buka file **`firebase-config.js`** 
2. Ganti isinya dengan config dari langkah 2 tadi

Contoh hasil akhir:
```js
const firebaseConfig = {
  apiKey: "AIzaSyAbC123...",
  authDomain: "borimmm-share.firebaseapp.com",
  databaseURL: "https://borimmm-share-default-rtdb.firebaseio.com",
  projectId: "borimmm-share",
  storageBucket: "borimmm-share.firebasestorage.app",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc123"
};
```

## 🌐 Cara Upload ke Hosting

Kalo gak punya web server, cara termudah:

### Opsi A: GitHub Pages (gratis)
1. Buat repo baru di https://github.com/ (nama: `borimmm-share`)
2. Upload semua file ke repo:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - `firebase-config.js`
3. Buka Settings > Pages > Source: `main` / root
4. Tunggu 2 menit, dapat URL: `https://username.github.io/borimmm-share/`

### Opsi B: Netlify (gratis, drag-and-drop)
1. Buka https://app.netlify.com/drop
2. Drag folder `Borimmm Share` ke browser
3. Dapat URL: `https://namacakaran.netlify.app/`

## 📱 Cara Pasang di iPhone Home Screen

1. Buka Safari, buka URL hasil upload
2. Klik tombol **Share** ( kotak dengan panah atas)
3. Scroll ke bawah, pilih **Add to Home Screen**
4. Nama akan terisi otomatis "Borimmm Share"
5. Klik **Add**
6. ✅ Selesai! Aplikasi muncul di home screen

**2 iPhone cara sama!** Tinggal buka URL yang sama di Safari masing-masing. Data otomatis sync lewat Firebase.

## 🎮 Cara Pakai
- **Tambah item**: tulis teks, pilih kategori, klik +
- **Centang**: klik lingkaran di kiri item
- **Hapus**: klik ✕ di kanan item
- **Filter**: tab di atas buat filter per kategori
- **Status**: liat koneksi di bawah — kalau ada 2 orang, muncul "♥ Aku & Pacar"

## 💡 Tips
- Pastikan 2 HP pakai URL yang SAMA
- Ada notifikasi "Tersambung" hijau di bawah kalo berhasil
- Kalo icon app cuma teks biasa, generate icon pake canva atau upload icon sendiri
