# Al-Quran Digital 📖

![Al-Quran Digital](https://img.shields.io/badge/Al--Quran-Digital-green.svg)
![HTML](https://img.shields.io/badge/HTML-5-orange.svg)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.0-blue.svg)

Mushaf Digital Indonesia - Aplikasi web modern untuk membaca Al-Quran dengan terjemahan bahasa Indonesia dan Inggris, dilengkapi dengan audio recitasi dari berbagai qari terkenal.

## ✨ Fitur Utama

- **📋 Daftar Surah Lengkap**: Menampilkan 114 surah dengan informasi detail
- **🎵 Audio Recitasi**: Multiple pilihan qari terkenal (Mishari Rashid, Abdur-Rahman as-Sudais, Saad al-Ghamdi)
- **🌍 Terjemahan Multi-bahasa**: Bahasa Indonesia dan Inggris
- **🎨 UI Modern**: Design responsif dengan glassmorphism effect
- **⌨️ Keyboard Navigation**: Navigasi dengan arrow keys (← →)
- **🔍 Debug Mode**: Panel debug untuk troubleshooting
- **📱 Responsive Design**: Optimized untuk desktop, tablet, dan mobile
- **🎯 Navigation Controls**: Tombol navigasi antar surah dengan preview
- **⚡ Progressive Loading**: Loading data secara bertahap
- **📂 Multiple Input Methods**: Load dari folder atau file manual

## 🚀 Demo

Kunjungi demo live: [Al-Quran Digital](https://musthofa-kamaluddin.github.io/Quran)

## 📋 Prerequisites

- Web browser modern (Chrome, Firefox, Safari, Edge)
- Web server lokal (untuk development)
- File JSON data surah (struktur dijelaskan di bawah)

## 🛠️ Instalasi

1. **Clone repository**
   ```bash
   git clone https://github.com/musthofa-kamaluddin/Quran.git
   cd Quran
   ```

2. **Struktur folder**
   ```
   Quran/
   ├── index.html
   ├── README.md
   └── surah/
       ├── 1.json
       ├── 2.json
       ├── 3.json
       └── ... (hingga 114.json)
   ```

3. **Jalankan dengan web server**
   ```bash
   # Menggunakan Python
   python -m http.server 8000
   
   # Menggunakan Node.js (http-server)
   npx http-server
   
   # Menggunakan PHP
   php -S localhost:8000
   ```

4. **Akses aplikasi**
   Buka browser dan akses `http://localhost:8000`

## 📊 Format Data JSON

Setiap file surah harus mengikuti struktur JSON berikut:

```json
{
  "name": "Al-Fatiha",
  "name_translations": {
    "ar": "الفاتحة",
    "en": "The Opening",
    "id": "Pembukaan"
  },
  "number_of_ayah": 7,
  "number_of_surah": 1,
  "place": "Mecca",
  "type": "Makkiyah",
  "recitations": [
    {
      "name": "Mishari Rashid al-`Afasy",
      "audio_url": "https://download.quranicaudio.com/quran/mishaari_raashid_al_3afaasee/001.mp3"
    }
  ],
  "verses": [
    {
      "number": 1,
      "text": "بِسْمِ ٱللَّهِ ٱلرَّحْمَٰنِ ٱلرَّحِيمِ",
      "translation_en": "In the name of Allah, the Entirely Merciful, the Especially Merciful.",
      "translation_id": "Dengan menyebut nama Allah Yang Maha Pemurah lagi Maha Penyayang."
    }
  ]
}
```

## 🎮 Cara Penggunaan

### Basic Navigation
- **Pilih Surah**: Klik pada card surah di halaman utama
- **Navigasi**: Gunakan tombol "Surah Sebelumnya" dan "Surah Selanjutnya"
- **Keyboard**: Tekan `←` atau `→` untuk navigasi cepat
- **Kembali**: Klik "Kembali ke Daftar Surah" atau tombol back

### Audio Controls
1. **Pilih Qari**: Gunakan dropdown untuk memilih reciter
2. **Play/Pause**: Klik tombol play di panel audio
3. **Progress**: Lihat progress audio pada progress bar

### Debug Mode
- Klik tombol "Debug Info" untuk melihat log aplikasi
- Berguna untuk troubleshooting masalah loading data

### Manual File Loading
Jika file tidak ditemukan secara otomatis:
1. Pilih "Gunakan Data Sample" untuk demo
2. Atau upload file JSON manual menggunakan file input

## 🔧 Konfigurasi

### Mengubah Jumlah Surah
```javascript
// Di dalam class QuranReader
this.maxSurah = 114; // Sesuaikan dengan jumlah surah yang tersedia
```

### Menambah Qari Baru
Tambahkan objek recitation baru dalam file JSON:
```json
{
  "name": "Nama Qari",
  "audio_url": "URL_AUDIO_MP3"
}
```

### Kustomisasi Style
File menggunakan Tailwind CSS dengan custom CSS tambahan:
- Font Arabic: Amiri
- Font Latin: Inter
- Color scheme: Green/Emerald theme

## 🛡️ Error Handling

Aplikasi menangani berbagai skenario error:
- **File tidak ditemukan**: Menampilkan opsi sample data atau manual upload
- **JSON invalid**: Log error detail di debug panel
- **Audio gagal load**: Fallback tanpa mengganggu functionality utama
- **Network issues**: Retry mechanism dan alternative loading methods

## 🤝 Contributing

1. Fork repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

### Guidelines
- Ikuti code style yang ada
- Test pada multiple browser
- Update dokumentasi jika diperlukan
- Pastikan responsive design tetap terjaga

## 📱 Browser Support

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🔗 Dependencies

- **Tailwind CSS**: Framework CSS utility-first
- **Lucide Icons**: Icon library modern
- **Google Fonts**: Amiri (Arabic) dan Inter (Latin)

Semua dependencies di-load dari CDN, tidak perlu instalasi tambahan.

## 👨‍💻 Author

**Musthofa Kamaluddin**
- GitHub: [@musthofa-kamaluddin](https://github.com/musthofa-kamaluddin)
- Website: https://luddin.my.id

## 🙏 Acknowledgments

- [QuranicAudio.com](https://quranicaudio.com) untuk audio recitasi
- [Tailwind CSS](https://tailwindcss.com) untuk framework CSS
- [Lucide](https://lucide.dev) untuk icon library
- Komunitas open source yang telah berkontribusi

## 📈 Roadmap

- [ ] Bookmark ayat favorit
- [ ] Search functionality
- [ ] Tema dark/light mode
- [ ] Offline support dengan Service Worker
- [ ] Mobile app (PWA)
- [ ] Tafsir integration
- [ ] Social sharing features

---

<div align="center">
  Made with ❤️ for the Ummah
</div>
