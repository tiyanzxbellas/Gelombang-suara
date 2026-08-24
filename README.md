# Gelombang Suara Studio (SoundWave Studio) 🌊🔊

Aplikasi web modern berbasis **Web Audio API & HTML5 Canvas** untuk:
1. **Membuka Gambar dari Suara & Mengubah Gambar menjadi Suara (Image ⇄ Sound)**.
2. **Mengubah Video menjadi Suara (Ekstrak Audio Asli & Sonifikasi Visual Video) serta Mengubah Suara menjadi Video (Video ⇄ Sound)**.
3. **Komunikasi Pesan Teks Offline via Gelombang Akustik (SoundChat MFSK)**.
4. **Studio Spektrogram Air Terjun (Real-Time Waterfall Spectrum & Audio Lab)**.

---

## 🚀 Fitur Utama

### 1. 🖼️ Gambar ⇄ Suara (Image ⇄ Sound)
- **Gambar Jadi Suara (Image to Sound)**:
  - **Upload Gambar** (PNG, JPG, WebP) atau **Gambar Langsung di Canvas** (Kuas, Penghapus, Teks, Preset).
  - Metode Sonifikasi:
    - **Visual Spektrogram (Additive Inverse FFT)**: Mengkodekan piksel gambar ke dalam spektrum frekuensi audio. Saat suara diputar di spektrum air terjun, gambar akan tampak secara visual!
    - **SSTV Robot36 Radio Scan**: Modulasi FM scanline radio amatir retro (sinkronisasi 1200Hz, scanline 1500–2300Hz).
    - **Stereo Harmonics**: Luminance dan kanal warna RGB dikonversi menjadi harmoni nada stereo (Left/Right).
  - Kontrol durasi (1.5s - 10s), rentang frekuensi (1kHz - 12kHz, 500Hz - 8kHz, 2kHz - 16kHz).
  - Putar langsung suara gambar, lihat waveform, dan **Download file audio `.WAV` 16-bit PCM**.
- **Buka Gambar dari Suara (Sound to Image)**:
  - **Buka File Audio**: Upload file `.WAV`, `.MP3`, atau `.OGG` untuk mendekode spektrum frekuensi audio menjadi gambar visual secara instan menggunakan FFT (Fast Fourier Transform).
  - **Dengarkan via Mikrofon (Real-Time Live Waterfall)**: Tangkap suara gambar yang diputar lewat speaker lain secara langsung di udara! Gambar akan tergambar otomatis di layar air terjun.
  - Palet Warna Spektrogram: *Inferno (Api)*, *Cyberpunk (Neon)*, *Viridis*, *Matrix CRT Hijau*, *Amber Retro*, dan *Grayscale*.
  - Ambil snapshot dan **Download Gambar Hasil Dekode (`.PNG`)**.

---

### 2. 🎬 Video ⇄ Suara (Video ⇄ Sound)
- **Video Jadi Suara (Video to Sound)**:
  - **Ekstrak Audio Asli Sumber Video**: Mengambil track audio murni yang tersimpan di dalam file video (MP4, WebM, MOV), visualisasi waveform, dan unduh sebagai file `.WAV`.
  - **Sonifikasi Visual Gerakan & Warna Video (Optical Sonification)**:
    - Menganalisis perubahan pergerakan frame (Motion Delta -> pitch bend), kecerahan (Luminance -> filter cutoff), dan distribusi warna RGB (Triad harmonic chords).
    - Menghasilkan soundscape dinamis yang menggambarkan suasana visual video secara real-time.
    - Opsi unduh file audio hasil sonifikasi video (`.WAV`).
- **Suara Jadi Video (Sound to Video Creator)**:
  - Mengubah file audio atau mikrofon menjadi video visual reaktif 2D/3D:
    - **Cymatics & Chladni Waves**: Pola resonansi simetris gelombang frekuensi suara.
    - **3D Spectral Terrain**: Lembah kawat 3D audio-reaktif.
    - **Laser Oscilloscope Lissajous**: Pancaran sinar vektor X-Y laser.
    - **Neon Quantum Equalizer**: Partikel kuantum dan cincin hologram menyala.
  - **Perekam Video Terintegrasi**: Rekam animasi visual canvas + audio track menjadi file video **`.WebM`** yang dapat langsung diunduh dan diputar.

---

### 3. 📻 SoundChat Teks (Acoustic Text Transceiver)
- Komunikasi teks offline tanpa Wi-Fi / Bluetooth menggunakan modulasi nada multi-frekuensi (MFSK).
- Pemancar nada (Transmitter) dan Penerima sinyal mikrofon real-time (Receiver).
- Pilihan kecepatan transmisi (Cepat, Standar, Akurat).
- Ekspor pesan teks ke file suara `.WAV` dan impor file audio pesan untuk didekodekan secara offline.

---

### 4. 🔬 Studio Spektrogram & Lab FFT (Live Waterfall & Lab)
- Spektrogram air terjun real-time resolusi tinggi (0 Hz - 22.05 kHz).
- Pelacak frekuensi puncak (*Peak Frequency Finder* dalam Hz).
- Generator nada uji (*Test Tones*, *Chirp Sweep*, *White Noise*, *Pink Noise*).

---

## 🛠️ Teknologi yang Digunakan
- **HTML5 & Vanilla ES6+ JavaScript**: Zero build step, ringan, dan cepat.
- **Web Audio API**: `AudioContext`, `AnalyserNode`, `OscillatorNode`, `BiquadFilterNode`, `MediaStreamDestination`, `OfflineAudioContext`.
- **Canvas API**: Rendering spektrogram berkecepatan tinggi dan visualisasi 2D/3D audio-reaktif.
- **MediaStream Recording API**: Perekaman video `.WebM` langsung dari browser.
- **Tailwind CSS & Lucide Icons**: Tampilan antarmuka modern bernuansa audio studio & cyberpunk yang responsif di desktop maupun mobile.

---

## 📖 Cara Menjalankan
Cukup buka file `index.html` di browser modern (Chrome, Edge, Firefox, Safari) atau jalankan server lokal:

```bash
# Menggunakan Python
python3 -m http.server 3000

# Atau menggunakan Node.js
npx serve .
```
Lalu buka `http://localhost:3000` di peramban web Anda.
