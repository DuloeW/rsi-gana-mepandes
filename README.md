# 💍 Digital Wedding Invitation — Bayu & Ayu

**Undangan Pernikahan Digital Premium**
Bayu Gelgel & Ayu Savitri · 20 Desember 2026

---

## ✨ Fitur

| Fitur | Keterangan |
|-------|-----------|
| 🎭 Opening Screen | Cover animasi sebelum undangan dibuka |
| 🏠 Hero Section | Nama, tanggal, dan tagline utama |
| 💑 Couple Profile | Profil kedua mempelai dengan foto |
| 📅 Event Details | Info akad & resepsi + tombol Maps |
| ⏱️ Countdown Timer | Hitung mundur real-time (WITA) |
| 📖 Our Story | Timeline perjalanan pasangan |
| 📸 Gallery | Grid foto + lightbox dengan swipe |
| 🎁 Wedding Gift | Nomor rekening + copy to clipboard |
| 📝 RSVP Form | Form konfirmasi + counter tamu |
| 💬 Guest Wishes | Ucapan tamu (localStorage) |
| 🎵 Music Player | Tombol play/pause floating |
| 🧭 Bottom Navigation | Floating nav glassmorphism |
| 🔔 Toast Notifications | Feedback interaksi user |

---

## 🗂️ Struktur Folder

```
undangan-nugraha/
│
├── index.html              ← Struktur HTML utama
│
├── css/
│   └── style.css           ← Semua styling (CSS Variables, responsive)
│
├── js/
│   └── script.js           ← Logic & interaksi (Vanilla JS)
│
├── assets/
│   ├── images/
│   │   ├── hero.jpg        ← Foto utama hero section
│   │   ├── groom.jpg       ← Foto pengantin pria
│   │   ├── bride.jpg       ← Foto pengantin wanita
│   │   ├── gallery-1.jpg   ← Foto gallery 1
│   │   ├── gallery-2.jpg   ← Foto gallery 2
│   │   ├── gallery-3.jpg   ← Foto gallery 3
│   │   ├── gallery-4.jpg   ← Foto gallery 4
│   │   ├── gallery-5.jpg   ← Foto gallery 5
│   │   ├── gallery-6.jpg   ← Foto gallery 6
│   │   ├── gallery-7.jpg   ← Foto gallery 7
│   │   └── gallery-8.jpg   ← Foto gallery 8
│   │
│   └── music/
│       └── background.mp3  ← Musik latar belakang
│
└── README.md               ← Dokumentasi ini
```

---

## 🚀 Cara Menjalankan

### Metode 1: Buka Langsung di Browser
```
Klik dua kali pada file index.html
```
> ⚠️ Beberapa fitur (musik, font Google) memerlukan koneksi internet.

### Metode 2: Live Server (Direkomendasikan)
Menggunakan VS Code dengan ekstensi **Live Server**:

1. Install ekstensi [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) di VS Code
2. Buka folder project di VS Code
3. Klik kanan `index.html` → **Open with Live Server**
4. Browser akan membuka `http://127.0.0.1:5500`

### Metode 3: Node.js HTTP Server
```bash
# Install serve globally
npm install -g serve

# Jalankan di folder project
serve .
```

### Metode 4: Python HTTP Server
```bash
# Python 3
python -m http.server 8080

# Buka browser: http://localhost:8080
```

---

## 🎨 Kustomisasi

### Mengubah Data Undangan
Edit file **`js/script.js`** bagian `invitationData`:

```javascript
const invitationData = {
    groom: {
        name: 'Nama Pengantin Pria',
        father: 'Nama Ayah',
        mother: 'Nama Ibu',
        instagram: 'https://instagram.com/username'
    },
    bride: {
        name: 'Nama Pengantin Wanita',
        father: 'Nama Ayah',
        mother: 'Nama Ibu',
        instagram: 'https://instagram.com/username'
    },
    wedding: {
        date: 'YYYY-MM-DD',          // Format: 2026-12-20
        displayDate: '20 Desember 2026',
    },
    ceremony: {
        venue: 'Nama Tempat Akad',
        address: 'Alamat Lengkap',
        mapsUrl: 'https://maps.google.com/?q=...'
    },
    reception: {
        venue: 'Nama Tempat Resepsi',
        address: 'Alamat Lengkap',
        mapsUrl: 'https://maps.google.com/?q=...'
    },
    bankAccounts: [
        {
            bank: 'Nama Bank',
            accountNumber: '0000000000',
            accountName: 'Nama Pemilik Rekening'
        }
    ]
};
```

### Mengubah Warna Tema
Edit file **`css/style.css`** bagian `:root`:

```css
:root {
    --primary-color: #8B6F47;       /* Warna utama (coklat emas) */
    --secondary-color: #D4AF78;     /* Warna aksen (emas terang) */
    --background-color: #FAF7F2;    /* Warna background */
    --text-color: #2C2416;          /* Warna teks utama */
}
```

### Menambah Foto
Letakkan foto di folder `assets/images/` dengan nama:
- `hero.jpg` — Foto utama
- `groom.jpg` — Foto pengantin pria
- `bride.jpg` — Foto pengantin wanita
- `gallery-1.jpg` s/d `gallery-8.jpg` — Foto gallery

**Ukuran yang direkomendasikan:**
- Hero: `1200 × 900px` (landscape)
- Couple: `600 × 800px` (portrait)
- Gallery: `800 × 800px` (square) atau bebas

### Menambah Musik
1. Letakkan file MP3 di `assets/music/background.mp3`
2. Format yang didukung: `.mp3`, `.ogg`, `.wav`
3. Edit `index.html` jika ingin mengganti path:
   ```html
   <source src="assets/music/background.mp3" type="audio/mpeg" />
   ```

---

## ⚙️ Teknologi

| Teknologi | Versi | Keterangan |
|-----------|-------|-----------|
| HTML5 | — | Semantic markup |
| CSS3 | — | CSS Variables, Grid, Flexbox, Animations |
| JavaScript | ES2020+ | Vanilla JS, IntersectionObserver, Clipboard API |
| Google Fonts | — | Playfair Display, Cormorant Garamond, Inter |
| Font Awesome | 6.5 | Icons |

---

## 📱 Browser Support

| Browser | Status |
|---------|--------|
| Chrome 88+ | ✅ Full support |
| Firefox 86+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Edge 88+ | ✅ Full support |
| Samsung Internet | ✅ Full support |

---

## 💡 Tips

1. **Performa**: Kompres foto sebelum diupload (gunakan [Squoosh](https://squoosh.app))
2. **Hosting**: Upload ke Netlify, Vercel, atau GitHub Pages secara gratis
3. **RSVP**: Data tersimpan di localStorage browser. Untuk backend, ganti fungsi `saveRSVP()` dan `getRSVPs()` di `script.js`
4. **Musik**: Gunakan format MP3 dengan bitrate 128kbps agar file tetap ringan

---

## 📤 Deploy ke Netlify (Gratis)

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login
netlify login

# Deploy
netlify deploy --prod --dir .
```

Atau drag & drop folder ke [app.netlify.com](https://app.netlify.com) 🚀

---

## 📜 Lisensi

Dibuat dengan ❤️ untuk **Bayu & Ayu**.
Bebas digunakan untuk keperluan pribadi.

---

*"Dan di antara tanda-tanda kekuasaan-Nya ialah Dia menciptakan untukmu istri-istri dari jenismu sendiri, supaya kamu cenderung dan merasa tenteram kepadanya."*
*— QS. Ar-Rum: 21*
