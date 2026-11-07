# DESIGN.md — YAN Portfolio

Arah desain resmi untuk portfolio YAN. File ini adalah sumber kebenaran visual; sebarang perubahan antarmuka harus konsisten dengan kontrak berikut.

## Identitas

- **Pemilik:** YAN, Android explorer & tech enthusiast.
- **Konsep:** kartu pengenal fisik (ID card / lanyard) yang digantung di ruang angkasa bernuansa anime (inspirasi K-ON! / Mio). Tema "identity card" ini adalah motif yang berulang: hero card, lanyard, dan aksen perangkat keras.
- **Suara:** Indonesia, personal, tenang, tidak kaku; hindari buzzword (pro "AI Powered", "Seamless", "Revolutionary").

## Palet

| Token | Nilai | Peran |
|---|---|---|
| `--bg` | `#030814` | dasar halaman (space) |
| `--panel` | `rgba(8,18,37,.72)` | permukaan kartu/panel |
| `--blue` | `#2677f5` | aksen utama (satu aksen disengaja) |
| `--blue2` | `#51a3ff` | varian terang aksen |
| `--white` | `#eef3ff` | teks utama |
| `--muted` | `#a1aec5` | teks sekunder |
| `--quiet` | `#6f7f9b` | teks tersier |

- Palet aktif: **2 inti (biru tua tua + biru aksen) + 1 netral (putih/abu)**. Tidak melebihi itu (R-29).
- Gradien hanya sebagai pemisah hierarki di lapisan dalam (kartu/lanyard), bukan sebagai latar seluruh halaman (R-01).

## Tipografi

| Peran | Font | Alasan |
|---|---|---|
| UI / body | Inter | keterbacaan antarmuka netral |
| Display / judul | Space Grotesk | karakter teknis-modern, diperuntukkan judul |
| Mono / label kecil | JetBrains Mono | label teknis (eyebrow, nomor) |

Pilihan ini didokumentasikan, bukan default tanpa alasan (R-06).

## Liquid Glass

- Glassmorphism dipakai sebagai **aksen**, bukan karakter seluruh UI (R-10). Dosis: **maksimal 1–2 elemen** — yaitu navigasi kapsul (navbar) dan menu mobile.
- Elemen lain (kartu proyek, panel kontak, kartu detail) tetap **solid**, dengan nuansa kaca hanya pada tepian (border/specular) tipis, bukan backdrop blur.
- Border-radius: sistem radius kecil yang disengaja (kotak ~10–16px, kapsul hanya pada navbar & badge). Tidak semua elemen berbentuk pil (R-11).
- Bayangan: dipakai sebagai penanda elevasi (kartu terangkat), bukan di semua elemen (R-12). Glow dibatasi pada 1–2 titik fokus (R-13).
- Kaca hanya boleh dipakai jika ada alasan hierarki; setiap pemakaian harus tercatat di sini.

## Dials

- **ENERGY 2** (balanced)
- **RHYTHM 2** (konsisten dengan beberapa variasi)
- **MOTION 2** (scroll-reveal, transisi; tidak ada loop tanpa akhir)

## Aturan anti-slop

- Tanpa emoji dekoratif di UI; ikon hanya bila relevan dan sebaiknya SVG (R-04).
- Tanpa panah `→`/`↗` pada tombol kecuali untuk tautan keluar yang memang perlu penanda arah (R-08).
- Tanpa statistik, testimoni, atau klaim palsu; konten ditulis dari fakta nyata (R-17, R-18, R-38).
- Setiap elemen interaktif memiliki fungsi nyata (R-26). Tautan navigasi menunjuk ke bagian yang benar-benar ada (R-24).
- Aksesibilitas: kontras WCAG AA, navigasi keyboard, dan `prefers-reduced-motion` dihormati (R-25, R-32, R-19).
- Semua media berukuran intrinsik; hero image tidak lazy (R-40).
