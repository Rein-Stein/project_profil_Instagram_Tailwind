# Instagram Clone - Tailwind CSS

Project ini adalah implementasi halaman profil Instagram sederhana menggunakan **Tailwind CSS (utility-first framework)**.  
Tujuan: menampilkan struktur halaman dengan header, bio, feed (minimal 12 gambar), dan footer yang responsif di berbagai ukuran layar.

---

## Pertanyaan README

### 1. Jelaskan keputusan grid-cols/gap di tiap breakpoint — kenapa begitu?
- **grid-cols-1 (default/mobile):** Supaya feed nyaman dilihat di layar kecil, foto ditampilkan satu per baris.
- **sm:grid-cols-2:** Di layar agak besar (tablet kecil), feed bisa ditampilkan 2 kolom biar lebih padat tapi tetap terbaca jelas.
- **md:grid-cols-3:** Mulai terasa seperti Instagram aslinya, feed lebih rapat dan seimbang.
- **lg:grid-cols-4:** Untuk desktop lebar, biar nggak terlalu kosong, jadi tampil 4 kolom.

> Intinya: semakin besar layar, semakin banyak kolom untuk memanfaatkan ruang tanpa mengorbankan keterbacaan.

### 2. Bagaimana kamu memanfaatkan utility responsive Tailwind untuk memecahkan masalah layout mobile di project ini?
- Menggunakan class **responsive prefix** (`sm:`, `md:`, `lg:`) untuk mengatur jumlah kolom grid.
- Mengatur urutan elemen dengan **order-1/order-2** supaya foto profil dan bio tampil sesuai di mobile vs desktop.
- Ukuran tombol dan teks pakai utility `text-sm md:text-base`, `px-2 md:px-4` agar nyaman di semua layar.

### 3. Jelaskan trade-off antara memakai banyak utility classes vs membuat CSS components tersendiri.
- **Utility classes (dipakai di project ini):**
  - Cepat, fleksibel, langsung bisa diatur per elemen.
  - Mudah responsif dengan prefix bawaan Tailwind.
  - Bisa bikin HTML panjang/berantakan kalau terlalu banyak.
- **Custom CSS components:**
  - Kode lebih rapih, class lebih pendek.
  - Reusable untuk elemen yang sama.
  - Lebih lambat buat eksperimen cepat, harus bikin aturan CSS manual.

> Trade-off: pakai utility lebih praktis untuk project kecil/cepat. Kalau project besar/kompleks, custom components lebih terstruktur.

---

## Fitur Tailwind yang digunakan
1. **Grid utilities** → `grid-cols-*` untuk mengatur jumlah kolom di berbagai breakpoint.  
2. **Flex utilities** → `flex`, `items-center`, `justify-center`, `gap-*`.  
3. **Order utilities** → `order-1`, `order-2` untuk mengatur urutan konten di mobile vs desktop.  
4. **Spacing utilities** → `p-*`, `m-*`, `gap-*` untuk padding, margin, dan jarak antar elemen.  

---


