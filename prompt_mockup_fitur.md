# Prompt Pembuatan Mockup Fitur — Google Form Arm Wrestling

> **Cara Pakai:** Berikan file `design.md` + salah satu prompt di bawah ini ke AI image/code generator.
> Setiap prompt menghasilkan 1 mockup fitur untuk dilampirkan di Google Form (Section 3 / Q12).

---

## Konteks Umum (Tempelkan Sebelum Setiap Prompt)

```
KONTEKS PROYEK:
Saya sedang membuat kuesioner Google Form untuk skripsi tentang platform digital komunitas arm wrestling (panco). Di dalam form ada bagian yang menampilkan 8 opsi fitur (3 fitur wajib + 5 fitur tambahan) yang bisa dipilih responden. Setiap fitur perlu 1 gambar mockup/wireframe agar responden memahami gambaran visual fiturnya sebelum memilih.

PANDUAN DESAIN:
- Baca dan ikuti design system dari file "design.md" yang saya lampirkan (Vercel-inspired design language)
- Baca dan ikuti panduan kualitas desain dari file "taste-SKILL.md" yang saya lampirkan (anti-slop frontend skill — berisi aturan layout, typography, color, motion, dan anti-pattern yang harus dihindari)
- Adaptasi kedua panduan tersebut untuk konteks APLIKASI WEB komunitas arm wrestling
- Gunakan font dan token warna sesuai yang tertulis di design.md
- Pastikan output tidak terlihat generic/templated — ikuti prinsip anti-default discipline dari taste-SKILL.md

FORMAT OUTPUT:
- Tampilan mobile-first (lebar 375px) — karena mayoritas responden isi form dari HP
- Mockup harus bersih, readable, dan mudah dipahami orang awam
- Sertakan header/navbar sederhana dengan nama app "ArmBase" dan ikon navigasi
- Tampilkan data dummy yang realistis untuk konteks arm wrestling Indonesia
- Output sebagai gambar PNG dengan resolusi tinggi (2x), background transparan atau gelap
```

---

## 🔶 FITUR TAMBAHAN (5 Fitur — Untuk Voting Q12)

---

## Prompt 1 — Tracking Latihan & Grafik Progres

```
Buatkan mockup UI mobile (375px width) untuk fitur "Tracking Latihan & Grafik Progres" di aplikasi arm wrestling bernama "ArmBase".

DESKRIPSI FITUR:
Fitur ini memungkinkan member mencatat latihan arm wrestling per sesi — termasuk jenis latihan, beban (kg), jumlah repetisi, dan set — sekaligus menampilkan grafik visual perkembangan kekuatan dari waktu ke waktu.

ELEMEN UI YANG HARUS ADA:
1. Header app "ArmBase" dengan ikon menu dan notifikasi
2. Judul halaman: "Catat & Pantau Latihan" dengan tanggal (contoh: Senin, 30 Juni 2026)
3. BAGIAN ATAS — Form Input Latihan:
   - Dropdown "Jenis Latihan" (contoh opsi: Wrist Curl, Pronation, Cupping, Hook Training, Top Roll Drill, Back Pressure)
   - Input "Beban" (contoh: 15 kg) dengan stepper +/-
   - Input "Repetisi" (contoh: 12 reps)
   - Input "Set" (contoh: 3 set)
   - Dropdown "Tangan" (Kiri / Kanan / Keduanya)
   - Tombol "Simpan Latihan" (primary button, warna #2b89ff)
4. Section "Latihan Hari Ini" yang menampilkan 2-3 card latihan yang sudah dicatat:
   - Card 1: "Wrist Curl — 15kg × 12 reps × 3 set (Kanan)"
   - Card 2: "Pronation — 10kg × 15 reps × 3 set (Keduanya)"
   - Card 3: "Cupping — 8kg × 20 reps × 2 set (Kiri)"
5. BAGIAN BAWAH — Grafik Progres Kekuatan:
   - Tab filter: "Minggu Ini" | "Bulan Ini" | "3 Bulan" (tab aktif = "Bulan Ini")
   - GRAFIK LINE CHART:
     - Sumbu X: tanggal (1 Jun — 30 Jun)
     - Sumbu Y: beban (kg)
     - 2 garis: Wrist Curl (warna #2b89ff) dan Pronation (warna #14c6cb)
     - Tren naik — menunjukkan progres positif
     - Tooltip di titik terakhir: "Wrist Curl: 18kg (+3kg dari awal bulan)"
   - 3 stat card kecil:
     - "Total Sesi: 14"
     - "Rata-rata Beban: 16.5 kg"
     - "Latihan Terfavorit: Wrist Curl"

GAYA VISUAL:
Ikuti design.md dan taste-SKILL.md. Pastikan mockup terlihat premium dan modern, bukan wireframe kasar.
Grafik dengan garis berwarna cerah di atas background gelap. Gunakan area fill transparan di bawah garis grafik.
```

---

## Prompt 2 — Panduan Pemula & Rekomendasi Program

```
Buatkan mockup UI mobile (375px width) untuk fitur "Panduan Pemula & Rekomendasi Program" di aplikasi arm wrestling bernama "ArmBase".

DESKRIPSI FITUR:
Halaman khusus untuk member baru yang berisi pengenalan dasar panco, tahapan belajar, dan rekomendasi menu latihan yang sesuai dengan style dominan mereka.

ELEMEN UI YANG HARUS ADA:
1. Header app "ArmBase"
2. Hero section kecil dengan judul: "Panduan & Rekomendasi" dan subjudul: "Belajar dari nol dan dapatkan program latihan sesuai style kamu"
3. BAGIAN ATAS — Tahapan Belajar Pemula:
   - Progress bar horizontal: "Tahap 1 dari 4" (25% terisi, warna #2b89ff)
   - 4 card tahapan vertikal (timeline style):
     - Tahap 1: "Postur & Grip Dasar" — "Pelajari cara berdiri, posisi siku, dan grip yang benar" — status: "Sedang Dipelajari" (aktif)
     - Tahap 2: "Mengenal 4 Style" — "Toproll, Hook, Press, Kingsmove — mana yang cocok?" — status: "Terkunci"
     - Tahap 3: "Latihan Dasar Pemula" — "Program 4 minggu untuk membangun fondasi kekuatan" — status: "Terkunci"
     - Tahap 4: "Siap Sparing Pertama" — "Tips dan mental preparation sebelum sparing" — status: "Terkunci"
   - Tombol "Mulai Tahap 1" (primary button)
4. BAGIAN BAWAH — Rekomendasi Program Latihan:
   - Section "Style Dominan Kamu" dengan 4 card pilihan style (grid 2×2):
     - "Toproll" (ikon: panah diagonal atas) — SELECTED/aktif, border biru #2b89ff
     - "Hook" (ikon: kait/hook)
     - "Press" (ikon: panah ke bawah)
     - "Kingsmove" (ikon: mahkota)
   - Badge "Style Aktif: Toproll"
   - Section "Program Latihan untuk Toproll" berisi 3 card rekomendasi latihan:
     - Card 1: "Pronation Drill" — "Melatih rotasi pergelangan ke dalam" — "3 set × 15 reps" — tag "Wajib"
     - Card 2: "Back Pressure" — "Membangun tarikan ke belakang" — "3 set × 12 reps" — tag "Utama"
     - Card 3: "Rising" — "Melatih gerakan naik saat toproll attack" — "4 set × 10 reps" — tag "Pendukung"
   - Tombol "Mulai Program Ini" (primary button biru)
5. Section kecil "Tips Keamanan" dengan ikon peringatan:
   - "Selalu pemanasan 10 menit sebelum sparing"
   - "Jangan pernah arm wrestling tanpa postur yang benar — risiko cedera tinggi"

GAYA VISUAL:
Ikuti design.md dan taste-SKILL.md. Timeline dengan garis vertikal yang menghubungkan tahapan.
Tahap aktif punya border accent yang jelas. Tahap terkunci punya opacity lebih rendah (0.5).
Tag "Wajib", "Utama", "Pendukung" menggunakan warna aksen yang berbeda-beda.
Tips keamanan gunakan warning card dengan border peringatan.
Card style yang aktif/selected harus punya border accent yang jelas.
```

---

## Prompt 3 — Pencari Lawan Sparing (Sparing Matcher)

```
Buatkan mockup UI mobile (375px width) untuk fitur "Pencari Lawan Sparing (Sparing Matcher)" di aplikasi arm wrestling bernama "ArmBase".

DESKRIPSI FITUR:
Member bisa mencari lawan sparing yang cocok berdasarkan berat badan, level, dan domisili kota.

ELEMEN UI YANG HARUS ADA:
1. Header app "ArmBase"
2. Judul halaman: "Cari Lawan Sparing"
3. Filter section dengan:
   - Dropdown "Berat Badan": "70–75 kg"
   - Dropdown "Level": "Menengah"
   - Dropdown "Kota": "Surabaya"
   - Tombol "Cari" (primary button biru)
4. Section "Lawan yang Cocok" — 3-4 card member:
   - Card 1: Avatar placeholder + "Raka Pratama" — "73 kg | Menengah | Toproll" — "Komunitas: ISPF Surabaya" — Badge "Online" (hijau) — Tombol "Ajak Sparing"
   - Card 2: Avatar + "Adi Surya" — "71 kg | Menengah | Hook" — "Komunitas: Panco Surabaya" — Badge "Terakhir aktif 2 jam lalu" (abu) — Tombol "Ajak Sparing"
   - Card 3: Avatar + "Budi Santoso" — "74 kg | Menengah | Press" — "Komunitas: ISPF Surabaya" — Badge "Online" (hijau) — Tombol "Ajak Sparing"
5. Setiap card menampilkan: foto/avatar, nama, berat badan, level, style dominan, komunitas, status online, dan CTA button

GAYA VISUAL:
Ikuti design.md dan taste-SKILL.md.
Badge "Online" gunakan warna hijau. Tombol "Ajak Sparing" secondary button.
Avatar bisa berupa circle placeholder dengan inisial nama.
```

---

## Prompt 4 — Riwayat & Ranking Supermatch

```
Buatkan mockup UI mobile (375px width) untuk fitur "Riwayat & Ranking Supermatch" di aplikasi arm wrestling bernama "ArmBase".

DESKRIPSI FITUR:
Menampilkan ranking/leaderboard member berdasarkan kategori berat badan, serta mencatat hasil supermatch dan sparing resmi komunitas.

ELEMEN UI YANG HARUS ADA:
1. Header app "ArmBase"
2. Tab atas: "Ranking" (aktif) | "Riwayat Supermatch"

TAB RANKING:
3. Dropdown filter: "Kategori: 70–75 kg" dan "Kota: Surabaya"
4. Podium visual top 3 (gaya medal):
   - 🥇 #1: "Raka Pratama" — Win: 12 | Loss: 2 — Skor: 1850
   - 🥈 #2: "Adi Surya" — Win: 10 | Loss: 3 — Skor: 1720
   - 🥉 #3: "Budi Santoso" — Win: 9 | Loss: 4 — Skor: 1650
5. List ranking #4 dan seterusnya:
   - #4: "Dimas Arifin" — Win: 8 | Loss: 5 — Skor: 1580
   - #5: "Fajar Hidayat" — Win: 7 | Loss: 5 — Skor: 1520

TAB RIWAYAT SUPERMATCH (tampilkan sebagai visual alternatif kecil di bawah, atau note):
6. 2-3 card riwayat supermatch:
   - "Raka Pratama vs Adi Surya — 3:1 (Best of 5) — 28 Jun 2026 — Kanan"
   - "Budi Santoso vs Dimas Arifin — 3:2 (Best of 5) — 25 Jun 2026 — Kanan"

GAYA VISUAL:
Ikuti design.md dan taste-SKILL.md. Podium top 3 bisa menggunakan aksen warna:
#1 gold, #2 silver, #3 bronze/coral — sesuaikan dengan palet di design.md.
```

---

## Prompt 5 — Panduan Pemulihan (Rehab) Cedera

```
Buatkan mockup UI mobile (375px width) untuk fitur "Panduan Pemulihan (Rehab) Cedera" di aplikasi arm wrestling bernama "ArmBase".

DESKRIPSI FITUR:
Halaman berisi informasi dan tips pemulihan nyeri sendi/tendon yang spesifik untuk olahraga arm wrestling (panco).

ELEMEN UI YANG HARUS ADA:
1. Header app "ArmBase"
2. Judul halaman: "Pemulihan & Rehab Cedera"
3. Subjudul: "Tips dan panduan pemulihan nyeri sendi & tendon spesifik untuk arm wrestling"
4. Section "Area Cedera Umum" — 4 card area tubuh (grid 2×2):
   - "Siku (Elbow)" — ikon siku — paling sering cedera
   - "Pergelangan Tangan (Wrist)" — ikon pergelangan
   - "Bahu (Shoulder)" — ikon bahu
   - "Jari & Telapak (Fingers)" — ikon tangan
   Setiap card: nama area + ikon sederhana, background surface-1
5. Section "Panduan Rehab: Siku (Elbow)" — setelah salah satu area dipilih:
   - Card 1: "Ice Therapy" — "Kompres es 15 menit setelah latihan berat" — ikon snowflake — tag "Pertolongan Pertama"
   - Card 2: "Peregangan Eksentrik" — "Wrist extension dengan beban ringan 2-3kg, 3 set × 15 reps" — tag "Rehabilitasi"
   - Card 3: "Istirahat Aktif" — "Hindari latihan berat 3-5 hari, lakukan gerakan ringan" — tag "Pemulihan"
6. Warning card di bawah:
   - ⚠️ "Jika nyeri tidak membaik setelah 1 minggu, segera konsultasi ke dokter atau fisioterapis. Jangan memaksakan latihan!"
7. Section kecil "Pencegahan Cedera":
   - "Selalu pemanasan 10-15 menit sebelum latihan/sparing"
   - "Gunakan teknik yang benar — postur buruk = cedera"
   - "Jangan naikkan beban terlalu drastis"

GAYA VISUAL:
Ikuti design.md dan taste-SKILL.md.
Tag "Pertolongan Pertama", "Rehabilitasi", "Pemulihan" menggunakan warna aksen yang berbeda-beda sesuai palet di design.md.
Warning card gunakan border peringatan dengan ikon peringatan.
Card area cedera yang dipilih/aktif punya border accent yang jelas.
```

---

## ✅ FITUR WAJIB (3 Fitur — Tidak untuk Voting, Hanya Penjelasan Visual)

---

## Prompt 6 — Kontak Pengurus Komunitas via WA

```
Buatkan mockup UI mobile (375px width) untuk fitur "Kontak Pengurus Komunitas via WA" di aplikasi arm wrestling bernama "ArmBase".

DESKRIPSI FITUR:
Akses instan untuk menghubungi ketua/senior komunitas arm wrestling setempat saat member siap bergabung — langsung via WhatsApp.

ELEMEN UI YANG HARUS ADA:
1. Header app "ArmBase"
2. Judul halaman: "Hubungi Pengurus Komunitas"
3. Subjudul: "Siap bergabung? Langsung hubungi ketua/senior komunitas terdekat via WhatsApp."
4. Filter dropdown: "Kota: Surabaya"
5. 3-4 card senior/ketua:
   - Card 1:
     - Avatar (inisial "HW") + Nama: "Hadi Wibowo"
     - Role badge: "Ketua ISPF Surabaya" (badge biru)
     - "Pengalaman: 8 tahun | Style: Toproll"
     - "Bisa bantu: Latihan, Event, Komunitas"
     - Tombol hijau WhatsApp: "Chat via WhatsApp" (background #25D366, ikon WA, rounded-md)
   - Card 2:
     - Avatar (inisial "SR") + "Surya Ramadhan"
     - Role badge: "Pelatih Senior" (badge cyan #14c6cb)
     - "Pengalaman: 6 tahun | Style: Hook"
     - "Bisa bantu: Teknik, Cedera/Rehab"
     - Tombol "Chat via WhatsApp"
   - Card 3:
     - Avatar (inisial "TP") + "Teguh Prasetyo"
     - Role badge: "Wakil Ketua ISPF Malang" (badge biru)
     - "Pengalaman: 5 tahun | Style: Press"
     - "Bisa bantu: Latihan, Sparing"
     - Tombol "Chat via WhatsApp"
6. Footer note kecil: "Hubungi di jam wajar ya (08.00–21.00). Senior juga manusia 😊"

GAYA VISUAL:
Ikuti design.md dan taste-SKILL.md.
Tombol WhatsApp harus sangat menonjol — gunakan warna hijau WhatsApp (#25D366) dengan ikon WA putih.
Role badge menggunakan rounded pill. Avatar circle dengan background subtle.
```

---

## Prompt 7 — Direktori Basecamp & Jadwal Latihan

```
Buatkan mockup UI mobile (375px width) untuk fitur "Direktori Basecamp & Jadwal Latihan" di aplikasi arm wrestling bernama "ArmBase".

DESKRIPSI FITUR:
Menampilkan peta/daftar lokasi latihan (basecamp) arm wrestling terdekat, ketersediaan meja panco standar, beserta jadwal rutin latihan mereka.

ELEMEN UI YANG HARUS ADA:
1. Header app "ArmBase"
2. Judul halaman: "Basecamp & Jadwal Latihan"
3. Subjudul: "Temukan lokasi latihan terdekat dan jadwal rutin mereka"
4. Filter dropdown: "Kota: Surabaya"
5. Mini-map placeholder di atas (area abu-abu dengan beberapa pin lokasi berwarna biru — tidak perlu detail peta)
6. 3 card basecamp:
   - Card 1 (HIGHLIGHT — border biru #2b89ff):
     - Nama: "Basecamp ISPF Surabaya"
     - 📍 "Jl. Raya Darmo No. 45, Surabaya"
     - 🪑 "Meja Panco: 3 meja standar tersedia"
     - 📅 "Jadwal Rutin: Senin, Rabu, Jumat — 19.00-21.00 WIB"
     - 👥 "Member aktif: 25 orang"
     - Badge "Terdekat" (hijau #00ca8e)
   - Card 2:
     - Nama: "GOR Pancoran Surabaya"
     - 📍 "Jl. Pancoran No. 12, Surabaya"
     - 🪑 "Meja Panco: 1 meja standar tersedia"
     - 📅 "Jadwal Rutin: Selasa, Kamis — 18.00-20.00 WIB"
     - 👥 "Member aktif: 12 orang"
   - Card 3:
     - Nama: "Basecamp Panco Sidoarjo"
     - 📍 "Jl. Ahmad Yani No. 88, Sidoarjo"
     - 🪑 "Meja Panco: 2 meja standar tersedia"
     - 📅 "Jadwal Rutin: Sabtu — 16.00-19.00 WIB"
     - 👥 "Member aktif: 18 orang"
7. Tombol "Lihat di Peta" (secondary button) di setiap card

GAYA VISUAL:
Ikuti design.md dan taste-SKILL.md.
Badge "Terdekat" gunakan warna hijau rounded pill.
Mini-map area bisa berupa rectangle dengan border halus dan pin dot.
```

---

## Prompt 8 — Papan Info Event & Lomba

```
Buatkan mockup UI mobile (375px width) untuk fitur "Papan Info Event & Lomba" di aplikasi arm wrestling bernama "ArmBase".

DESKRIPSI FITUR:
Papan pengumuman dan kalender lomba arm wrestling lokal maupun nasional — termasuk tanggal, lokasi, kategori, dan cara daftar — agar member tidak ketinggalan info.

ELEMEN UI YANG HARUS ADA:
1. Header app "ArmBase"
2. Judul halaman: "Event & Lomba"
3. Tab: "Mendatang" (aktif) | "Selesai"
4. 3 card event:
   - Card 1 (HIGHLIGHT — border biru #2b89ff):
     - Badge "Mendatang" (biru)
     - Judul: "Kejuaraan Nasional Arm Wrestling 2026"
     - 📅 "15–16 Agustus 2026"
     - 📍 "GOR Sidoarjo, Jawa Timur"
     - 🏋️ "Kategori: U-65, U-70, U-75, U-80, U-90, +90 kg"
     - Tombol "Lihat Detail & Daftar" (primary)
   - Card 2:
     - Badge "Mendatang" (biru)
     - "Supermatch Surabaya Open"
     - 📅 "20 Juli 2026"
     - 📍 "Basecamp ISPF Surabaya"
     - 🏋️ "Kategori: Bebas (challenge system)"
     - Tombol "Lihat Detail" (secondary)
   - Card 3:
     - Badge "1 Minggu Lagi" (kuning/warning)
     - "Sparing Akbar Komunitas Panco Jatim"
     - 📅 "7 Juli 2026"
     - 📍 "Taman Bungkul, Surabaya"
     - 🏋️ "Kategori: Pemula, Menengah, Kompetitif"
     - Tombol "Lihat Detail" (secondary)

GAYA VISUAL:
Ikuti design.md dan taste-SKILL.md. Badge event menggunakan rounded pill.
Card event highlight (terdekat) punya subtle border accent.
```

---

## Tips Penggunaan Prompt

> [!TIP]
> **Cara pakai di AI:**
> 1. Copy **Konteks Umum** (bagian paling atas)
> 2. Paste di awal prompt
> 3. Tambahkan **salah satu prompt fitur** (Prompt 1–8) di bawahnya
> 4. Lampirkan file `design.md` sebagai referensi desain
> 5. Generate — review — revisi jika perlu

> [!IMPORTANT]
> **Urutan pembuatan yang disarankan:**
> Mulai dari fitur tambahan (yang akan di-voting Q12) karena paling penting secara visual:
> 1. **Prompt 1** (Tracking & Grafik Progres) — paling visual, ada form + chart
> 2. **Prompt 4** (Ranking Supermatch) — leaderboard/tabel
> 3. **Prompt 2** (Panduan & Rekomendasi) — timeline + style cards
> 4. **Prompt 3** (Sparing Matcher) — filter + member cards
> 5. **Prompt 5** (Rehab Cedera) — area tubuh + panduan
> 6. Lalu fitur wajib: **Prompt 6** → **Prompt 7** → **Prompt 8**

> [!NOTE]
> **Pemetaan Fitur ke Masalah Q8/Q9:**
>
> | # | Fitur (Prompt) | Masalah yang Dijawab |
> |---|---|---|
> | 1 | Tracking Latihan & Grafik Progres | Latihan terasa tidak terukur & sulit memantau perkembangan |
> | 2 | Panduan Pemula & Rekomendasi Program | Bingung program latihan yang cocok |
> | 3 | Pencari Lawan Sparing | Susah mencari lawan sparing yang selevel |
> | 4 | Riwayat & Ranking Supermatch | Tidak adanya catatan resmi hasil tanding |
> | 5 | Panduan Pemulihan (Rehab) Cedera | Khawatir cedera atau bingung cara pemulihan |
> | 6 | Kontak Pengurus Komunitas via WA | Tidak tahu kontak senior/pengurus untuk bergabung |
> | 7 | Direktori Basecamp & Jadwal Latihan | Sulit mencari info lokasi basecamp & jadwal |
> | 8 | Papan Info Event & Lomba | Sering telat mendapatkan info lomba/event |

> [!NOTE]
> **Setelah semua mockup jadi:**
> Simpan semua gambar PNG di folder:
> `02_Requirement_Gathering/mockup_fitur_gform/`
> dengan format penamaan:
> - `01_tracking_grafik_progres.png`
> - `02_panduan_pemula_rekomendasi.png`
> - `03_pencari_lawan_sparing.png`
> - `04_riwayat_ranking_supermatch.png`
> - `05_panduan_rehab_cedera.png`
> - `06_kontak_pengurus_wa.png`
> - `07_direktori_basecamp_jadwal.png`
> - `08_papan_info_event_lomba.png`
