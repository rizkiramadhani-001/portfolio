# DESIGN.md — acuan bikin website

Hasil distilled dari sesi portofolio Rizki (Nov 2026). Versi referensi: `portfolio-rizki/lengkap.html` (edisi yang diadopsi dari Claude). Baca file ini dulu sebelum bikin website baru.

## Prinsip utama

1. Signature dulu, template belakangan. Setiap halaman wajib punya satu benda yang hanya bisa dimiliki produk ini (contoh: monitor drum simulasi untuk portofolio IoT). Kalau logo dan nama diganti lalu desain tetap terasa sama, desainnya gagal.
2. Motion meniru perilaku produk, bukan hiasan. Pulse untuk status live, hop untuk alur data, typewriter untuk peran. Semua animasi: konten tetap terbaca tanpa JS, dan mati total di `prefers-reduced-motion`.
3. Jujur soal data. Angka simulasi wajib dilabeli (contoh: "simulated signal, not live farm data"). Tidak ada metrik, testimoni, atau demo yang diada-adakan.

## Sistem visual (night-ops)

- Token di `:root`, tidak ada warna atau font literal di luar token: `--bg #0B1413`, `--panel #132220`, `--ink #EAF2EE`, `--soft #C3D4CD`, `--muted #93A8A0`, `--line #23403A`, `--accent #3FE0BE`, plus `--amber #F5B544` hanya untuk semantik juara/pencapaian.
- Font: Bricolage Grotesque (display, ekspresif, hindari default AI), Public Sans (body), IBM Plex Mono (label dan data).
- Tekstur grid hero selalu di-mask radial agar tidak menenggelamkan konten. Tidak ada gradient ungu-biru, tidak ada glow di mana-mana.
- Komposisi bervariasi per section: hero split, strip alur, grid timpang, index baris ledger, definition rows. Jangan semua section berupa kartu seragam.

## Copywriting

- Tanpa em dash. Kalimat aktif dengan aktor jelas ("I built"). Satu ide problem-first per proyek: masalah dulu, baru yang dibangun.
- CTA spesifik ("Email me about an internship"), bukan "Get Started". Tanpa buzzword (seamless, cutting-edge, revolutionary).

## Fungsional (wajib jalan)

- Sticky header + scrollspy, tombol copy-to-clipboard dengan feedback, link CV PDF, semua anchor menunjuk ke section yang ada.
- Print stylesheet: semua konten harus muncul di PDF (hati-hati dengan elemen `opacity: 0` dari efek reveal).

## Gate sebelum serah terima

- 0 em dash, 0 middle-dot meta, 0 panah hias, 0 gradient, kontras teks AA, fokus keyboard terlihat, tidak ada kontrol mati.
