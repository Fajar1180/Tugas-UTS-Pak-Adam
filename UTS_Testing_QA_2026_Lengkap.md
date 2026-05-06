# UJIAN TENGAH SEMESTER  
## MATA KULIAH: SOFTWARE TESTING & QUALITY ASSURANCE  

**Program Studi**: Sistem Informasi  
**Sifat**: Online  
**Waktu Pengerjaan**: 2 Minggu  

**Nama**: ........................................  
**NIM**: ........................................  
**Kelas**: ........................................  

---

# Soal 1. Pemahaman Testing dan Quality Assurance Berbasis Kasus (Bobot 20)

**Kasus singkat**:  
Tim mengembangkan Sistem Informasi Perpustakaan berbasis web. Masalah yang muncul: kebutuhan pengguna belum terdokumentasi lengkap, tidak ada standar penulisan requirement, developer langsung bikin fitur tanpa review dokumen, belum ada format baku test case, UI membingungkan, dan testing baru mau dilakukan mendekati implementasi tanpa QA dari awal.

---

## 1) Perbedaan QA, QC, dan Testing

Menurut saya, QA, QC, dan testing itu sama-sama untuk kualitas, tapi fokusnya beda:

- **Quality Assurance (QA)**: fokus ke *proses* dan sifatnya pencegahan. QA memastikan dari awal cara kerja tim sudah benar (standar requirement, proses review, standar dokumentasi, standar pengujian, dsb), supaya defect tidak banyak muncul belakangan.

- **Quality Control (QC)**: fokus ke *produk/hasil kerja*. QC mengecek apakah output (dokumen, modul, fitur) sudah sesuai standar atau belum, biasanya lewat review, audit, checklist, dan verifikasi.

- **Testing**: bagian dari QC yang fokus menjalankan sistem/aplikasi untuk menemukan bug atau ketidaksesuaian (functional test, UI test, performance test, dll).

Kalau disimpulkan: **QA = pencegahan lewat proses**, **QC = kontrol kualitas hasil**, **Testing = aktivitas pengujian untuk menemukan defect**.

---

## 2) Identifikasi minimal 4 masalah kualitas pada kasus

Masalah kualitas yang terlihat dari kasus tersebut, menurut saya:

1. **Requirement tidak lengkap dan dokumentasi kebutuhan lemah** → rawan salah implementasi.
2. **Tidak ada standar penulisan requirement** → dokumen kebutuhan tidak konsisten dan sulit direview.
3. **Fitur dibuat tanpa review dokumen** → tidak ada quality gate sebelum coding.
4. **Tidak ada format baku test case** → pengujian tidak konsisten dan sulit ditelusuri (traceability rendah).
5. **UI membingungkan** → masalah usability (navigasi, label, layout tidak intuitif).
6. **Testing baru dilakukan di akhir** → risiko bug menumpuk dan biaya perbaikan makin besar.

---

## 3) Aktivitas/tahapan QA yang seharusnya dilakukan sejak awal

Aktivitas QA yang sebaiknya dilakukan sejak awal agar masalah bisa dicegah:

- **Standarisasi requirement**
  - bikin template requirement (mis. SRS/URD sederhana),
  - definisikan standar bahasa/format (jelas, tidak ambigu, testable),
  - lakukan *requirement review* rutin dengan user dan tim.

- **Quality gate sebelum coding**
  - review requirement dan desain sebelum implementasi,
  - minimal lakukan checklist kelengkapan requirement.

- **Test planning sejak awal**
  - susun Test Plan (scope, jenis testing, jadwal, tools, risiko),
  - tentukan kriteria penerimaan (acceptance criteria).

- **Standarisasi test case**
  - gunakan template test case yang sama (mis. format Katalon/IEEE),
  - kaitkan requirement dengan test case (traceability).

- **Evaluasi usability lebih awal**
  - buat prototype/wireframe,
  - lakukan feedback cepat dari beberapa user.

---

## 4) Dampak jika hanya fokus testing di akhir tanpa QA memadai sejak awal

Dampaknya yang mungkin terjadi:

- **Bug dan mismatch requirement baru ketahuan telat**, sehingga revisi lebih mahal dan makan waktu.
- **Jadwal implementasi berisiko molor**, karena perbaikan di akhir sering berantai.
- **UI/UX susah dibenahi** kalau struktur aplikasi sudah terlanjur jadi.
- **Dokumentasi & test case kurang rapi**, bikin maintenance setelah live makin susah.
- **Risiko kegagalan implementasi meningkat** karena user tidak puas/fitur tidak sesuai kebutuhan.

---

# Soal 2. Analisis McCall Quality Model Berdasarkan Data Mentah (Bobot 40)

## A. Identifikasi dari narasi kasus
1. **Objek evaluasi**: Sistem Informasi Akademik (SIAKAD) (login, KRS, KHS, input nilai dosen, sinkronisasi pembayaran).  
2. **Sumber data**:
   - Kuantitatif: 5 evaluator internal (skala Likert 1–5) untuk tiap indikator.
   - Kualitatif: wawancara singkat, observasi, audit dokumen, ringkasan log sistem.
3. **Faktor McCall yang digunakan**:
   - correctness, reliability, efficiency, usability, maintainability, interoperability.
4. **Indikator**:
   - Correctness: C1, C2, C3  
   - Reliability: R1, R2, R3  
   - Efficiency: E1, E2, E3  
   - Usability: U1, U2, U3  
   - Maintainability: M1, M2, M3  
   - Interoperability: I1, I2, I3  

---

## B. Perhitungan skor rata-rata indikator (Ci)
Rumus: **Ci = (jumlah skor evaluator) / (jumlah evaluator)**, evaluator = 5.

### 1) Correctness
- **C1** = (4+4+5+4+4) / 5 = 21/5 = **4,20**  
- **C2** = (4+4+4+4+4) / 5 = 20/5 = **4,00**  
- **C3** = (4+4+4+3+4) / 5 = 19/5 = **3,80**

### 2) Reliability
- **R1** = (3+3+3+3+4) / 5 = 16/5 = **3,20**  
- **R2** = (3+3+2+3+3) / 5 = 14/5 = **2,80**  
- **R3** = (3+3+3+3+3) / 5 = 15/5 = **3,00**

### 3) Efficiency
- **E1** = (3+3+3+4+3) / 5 = 16/5 = **3,20**  
- **E2** = (3+3+3+2+3) / 5 = 14/5 = **2,80**  
- **E3** = (3+3+3+3+3) / 5 = 15/5 = **3,00**

### 4) Usability
- **U1** = (3+4+3+4+3) / 5 = 17/5 = **3,40**  
- **U2** = (3+3+3+4+3) / 5 = 16/5 = **3,20**  
- **U3** = (3+3+3+3+3) / 5 = 15/5 = **3,00**

### 5) Maintainability
- **M1** = (2+2+3+2+3) / 5 = 12/5 = **2,40**  
- **M2** = (2+2+2+3+2) / 5 = 11/5 = **2,20**  
- **M3** = (2+2+2+2+2) / 5 = 10/5 = **2,00**

### 6) Interoperability
- **I1** = (3+3+3+3+3) / 5 = 15/5 = **3,00**  
- **I2** = (3+2+3+3+2) / 5 = 13/5 = **2,60**  
- **I3** = (3+3+3+2+3) / 5 = 14/5 = **2,80**

---

## C. Skor faktor berbobot (Fa), persentase faktor (Pa), dan gap
Rumus:
- **Fa = Σ (wi × Ci)**  
- **Pa = (Fa/5) × 100%**  
- **Gap = 5 − Fa**

### 1) Correctness (w: 0,35; 0,35; 0,30)
Fa = (0,35×4,20) + (0,35×4,00) + (0,30×3,80)  
= 1,47 + 1,40 + 1,14  
= **4,01**  

Pa = (4,01/5)×100% = **80,20%** → **Baik**  
Gap = 5 − 4,01 = **0,99** → **Kecil**

### 2) Reliability (w: 0,35; 0,35; 0,30)
Fa = (0,35×3,20) + (0,35×2,80) + (0,30×3,00)  
= 1,12 + 0,98 + 0,90  
= **3,00**  

Pa = (3,00/5)×100% = **60,00%** → **Cukup**  
Gap = 5 − 3,00 = **2,00** → **Sedang**

### 3) Efficiency (w: 0,40; 0,35; 0,25)
Fa = (0,40×3,20) + (0,35×2,80) + (0,25×3,00)  
= 1,28 + 0,98 + 0,75  
= **3,01**  

Pa = (3,01/5)×100% = **60,20%** → **Cukup**  
Gap = 5 − 3,01 = **1,99** → **Sedang**

### 4) Usability (w: 0,35; 0,35; 0,30)
Fa = (0,35×3,40) + (0,35×3,20) + (0,30×3,00)  
= 1,19 + 1,12 + 0,90  
= **3,21**  

Pa = (3,21/5)×100% = **64,20%** → **Baik**  
Gap = 5 − 3,21 = **1,79** → **Sedang**

### 5) Maintainability (w: 0,35; 0,35; 0,30)
Fa = (0,35×2,40) + (0,35×2,20) + (0,30×2,00)  
= 0,84 + 0,77 + 0,60  
= **2,21**  

Pa = (2,21/5)×100% = **44,20%** → **Cukup**  
Gap = 5 − 2,21 = **2,79** → **Besar**

### 6) Interoperability (w: 0,40; 0,30; 0,30)
Fa = (0,40×3,00) + (0,30×2,60) + (0,30×2,80)  
= 1,20 + 0,78 + 0,84  
= **2,82**  

Pa = (2,82/5)×100% = **56,40%** → **Cukup**  
Gap = 5 − 2,82 = **2,18** → **Sedang**

---

## D. Skor keseluruhan (Q), persentase (Q%), dan gap keseluruhan
Asumsi bobot antarfaktor sama: **Wf = 1/6**.

Q = (4,01 + 3,00 + 3,01 + 3,21 + 2,21 + 2,82) / 6  
= 18,26 / 6  
= **3,04**

Q% = (3,04/5)×100% = **60,87%**  
Gap keseluruhan = 5 − 3,04 = **1,96**

**Kategori kualitas keseluruhan**: **Cukup** (60,87% masih sedikit di bawah 61%, jadi belum masuk Baik)  
**Kategori gap keseluruhan**: **Sedang**

---

## E. Prioritas perbaikan (paling mendesak → paling rendah)
Berdasarkan gap dan dampak layanan, menurut saya urutan prioritasnya:

1. **Maintainability** (gap 2,79 – besar)  
2. **Interoperability** (gap 2,18 – sedang; terkait pembayaran)  
3. **Reliability** (gap 2,00 – sedang; timeout saat jam sibuk)  
4. **Efficiency** (gap 1,99 – sedang; performa melambat saat padat)  
5. **Usability** (gap 1,79 – sedang; masih bisa dipakai tapi perlu perbaikan)  
6. **Correctness** (gap 0,99 – kecil; relatif paling baik)

---

## F. Interpretasi kualitatif (berdasarkan temuan lapangan)
- **Correctness** cukup tinggi karena fitur inti (KRS/KHS) umumnya sesuai kebutuhan, tapi ada mismatch kecil status pembayaran vs kelayakan KRS dan ringkasan nilai pernah telat update.  
- **Reliability** sedang karena pada periode KRS terjadi timeout dan transaksi perubahan KRS harus diulang, serta log menunjukkan error meningkat saat trafik tinggi.  
- **Efficiency** sedang karena dashboard dan beberapa pencarian terasa lambat saat jam padat, dan query laporan meningkat saat banyak user akses bersamaan.  
- **Usability** sudah lumayan, tapi label menu kurang intuitif, tampilan mobile sempit di beberapa halaman, dan pesan error belum membantu.  
- **Maintainability** paling rendah karena dokumentasi teknis belum lengkap, tracing bug masih bergantung pada satu developer, dan keterkaitan antar modul tinggi.  
- **Interoperability** masih bermasalah di sinkron pembayaran yang beberapa kali terlambat, serta dokumentasi integrasi belum rinci untuk audit/troubleshooting.

---

## G. Rekomendasi perbaikan (minimal 3)
1. **Fokus maintainability**
   - lengkapi dokumentasi teknis (arsitektur, alur KRS/KHS, skema DB, daftar API),
   - buat SOP release + changelog,
   - knowledge sharing supaya tracing bug tidak tergantung 1 orang.

2. **Perkuat reliability dan efficiency saat jam sibuk**
   - lakukan load test/stress test khusus periode KRS,
   - optimasi query (indexing, caching, pagination),
   - monitoring performa (response time, error rate) dan alerting.

3. **Perbaiki interoperability integrasi pembayaran**
   - tetapkan mekanisme sinkron yang jelas (mis. queue/event atau scheduler dengan SLA),
   - buat audit log integrasi untuk tracing transaksi yang terlambat,
   - perjelas dokumentasi integrasi untuk kebutuhan audit dan troubleshooting.

4. **Benahi usability**
   - perbaiki label menu, tambah bantuan/tooltips,
   - rapikan responsive design untuk mobile khususnya halaman form,
   - perbaiki pesan error agar lebih informatif (apa salahnya dan apa yang harus dilakukan).

---

# Soal 3. Desain Test Case Berdasarkan Testing Challenges #1–#2 (Bobot 40)

## A. Challenge #1 – Web Testing (Field: First Name, Max Length 30)
**Link:** http://testingchallenges.thetestingmap.org/  
**Fokus pengujian:** hanya field **First Name** sesuai spesifikasi di halaman.

| ID Test Case | Nama Skenario | Preconditions | Langkah Uji | Data Uji | Hasil yang Diharapkan |
|---|---|---|---|---|---|
| TC-CH1-01 | Empty value (nilai kosong) | Halaman Challenge #1 terbuka | 1) Kosongkan First Name 2) Klik Submit | (kosong) | Sistem mendeteksi input kosong (check *Empty value* terpenuhi), form ditolak/validasi muncul |
| TC-CH1-02 | Space (hanya spasi) | Halaman Challenge #1 terbuka | 1) Isi First Name dengan spasi saja 2) Submit | `" "` | Sistem mendeteksi input spasi (check *Space* terpenuhi) |
| TC-CH1-03 | Space values at the beginning | Halaman Challenge #1 terbuka | 1) Isi First Name ada spasi di awal 2) Submit | `" Fajar"` | Sistem mendeteksi spasi di awal (check terpenuhi) |
| TC-CH1-04 | Space values at the end | Halaman Challenge #1 terbuka | 1) Isi First Name ada spasi di akhir 2) Submit | `"Fajar "` | Sistem mendeteksi spasi di akhir (check terpenuhi) |
| TC-CH1-05 | Space in the middle | Halaman Challenge #1 terbuka | 1) Isi First Name 2 kata 2) Submit | `"Fajar Putra"` | Sistem mendeteksi spasi di tengah (check terpenuhi) |
| TC-CH1-06 | Other chars then alphabetic | Halaman Challenge #1 terbuka | 1) Isi First Name dengan angka/simbol 2) Submit | `"Fajar123"` / `"Fajar!"` | Sistem mendeteksi karakter non-alfabet (check terpenuhi) |
| TC-CH1-07 | Non ASCII | Halaman Challenge #1 terbuka | 1) Isi First Name karakter non-ASCII 2) Submit | `"Fajaré"` / `"测试"` | Sistem mendeteksi karakter non-ASCII (check terpenuhi) |
| TC-CH1-08 | You used HTML tags | Halaman Challenge #1 terbuka | 1) Isi First Name dengan tag HTML 2) Submit | `"<b>Fajar</b>"` | Sistem mendeteksi tag HTML (check terpenuhi) |
| TC-CH1-09 | Basic XSS | Halaman Challenge #1 terbuka | 1) Isi payload XSS 2) Submit | `"<script>alert(1)</script>"` | Sistem mendeteksi XSS basic (check terpenuhi). Idealnya script tidak dieksekusi |
| TC-CH1-10 | Basic SQL injection | Halaman Challenge #1 terbuka | 1) Isi payload SQLi 2) Submit | `"' OR '1'='1"` | Sistem mendeteksi SQL injection basic (check terpenuhi). Idealnya tidak terjadi bypass |
| TC-CH1-11 | You looked at the page source | Halaman Challenge #1 terbuka | 1) Klik kanan → View Page Source 2) Lihat source | - | Check *You looked at the page source* terpenuhi |
| TC-CH1-12 | You looked at the cookie | Halaman Challenge #1 terbuka | 1) F12 2) Application/Storage → Cookies 3) Lihat cookie | - | Check *You looked at the cookie* terpenuhi |
| TC-CH1-13 | Missing CSS | Halaman Challenge #1 terbuka | 1) F12 → Network 2) Block/disable CSS 3) Refresh | - | CSS tidak ter-load (tampilan tanpa styling), check *Missing CSS* terpenuhi |
| TC-CH1-14 | You made the user admin | Sudah ada session/cookie | 1) F12 → Cookies/Storage 2) Cari value role 3) Ubah jadi admin 4) Refresh | role=user → admin (jika ada) | Check *You made the user admin* terpenuhi |
| TC-CH1-15 | Minimum value (panjang minimum) | Halaman Challenge #1 terbuka | 1) Isi 1 karakter 2) Submit | `"A"` | Sistem mendeteksi minimum length (check *Minimum value* terpenuhi) |
| TC-CH1-16 | Average value (nilai normal) | Halaman Challenge #1 terbuka | 1) Isi nama normal 2) Submit | `"Fajar"` | Sistem mendeteksi nilai normal (check *Average value* terpenuhi) |
| TC-CH1-17 | Maximum values (30 karakter) | Halaman Challenge #1 terbuka | 1) Isi 30 karakter 2) Submit | `"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"` (30) | Sistem mendeteksi batas maksimum (check *Maximum values* terpenuhi) |
| TC-CH1-18 | More than maximum values (31+ karakter) | Halaman Challenge #1 terbuka | 1) Isi 31 karakter 2) Submit | `"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"` (31) | Sistem menolak/memotong input, check *More than maximum values* terpenuhi |

---

## B. Challenge #2 – Bypass HTML5 Validations
**Link:** http://testingchallenges.thetestingmap.org/challenge2.php  
**Tujuan challenge:** bypass validasi HTML5 pada input angka dengan cara inspect dan mengubah `type="number"` menjadi `type="text"` agar bisa input selain integer.

| ID Test Case | Nama Skenario | Preconditions | Langkah Uji | Data Uji | Hasil yang Diharapkan |
|---|---|---|---|---|---|
| TC-CH2-01 | Validasi HTML5 aktif: huruf ditolak (type=number) | Halaman Challenge #2 terbuka, field target masih `type=number` | 1) Klik field 2) Input huruf 3) Klik Send name | `abc` | Browser menolak/validasi muncul, form tidak terkirim |
| TC-CH2-02 | Validasi HTML5 aktif: simbol ditolak (type=number) | Field masih `type=number` | 1) Isi simbol 2) Submit | `@#$` | Validasi HTML5 muncul, submit gagal |
| TC-CH2-03 | Baseline: integer diterima (type=number) | Field masih `type=number` | 1) Isi integer 2) Isi Name 3) Isi captcha 4) Submit | angka `10`, Name `Fajar`, captcha benar | Form terkirim (lolos validasi client) |
| TC-CH2-04 | Bypass: ubah type number → text via Inspect | Halaman terbuka, DevTools bisa dipakai | 1) F12 2) Inspect field 3) Ubah `type="number"` jadi `type="text"` | - | Field menerima input non-integer (validasi HTML5 tidak membatasi lagi) |
| TC-CH2-05 | Setelah bypass: input huruf bisa disubmit | Type sudah `text` | 1) Isi field dengan huruf 2) Isi Name + captcha 3) Submit | `abc`, Name `Fajar`, captcha benar | Request bisa terkirim (tidak ditahan HTML5). Respon sistem dicatat |
| TC-CH2-06 | Setelah bypass: input alfanumerik | Type sudah `text` | 1) Isi campuran angka+huruf 2) Submit | `12A3` | Request terkirim, sistem merespon sesuai validasi server-side |
| TC-CH2-07 | Setelah bypass: input desimal titik | Type sudah `text` | 1) Isi desimal 2) Submit | `10.5` | Request terkirim. Jika harus integer, idealnya ditolak oleh server |
| TC-CH2-08 | Setelah bypass: input desimal koma (locale) | Type sudah `text` | 1) Isi desimal koma 2) Submit | `10,5` | Request terkirim, bisa ditolak/di-parse tergantung setting |
| TC-CH2-09 | Setelah bypass: thousand separator | Type sudah `text` | 1) Isi angka ribuan 2) Submit | `1,000` / `1.000` | Request terkirim, sistem merespon sesuai parsing/aturan server |
| TC-CH2-10 | Setelah bypass: spasi di awal/akhir | Type sudah `text` | 1) Isi angka dengan spasi 2) Submit | `" 10"` dan `"10 "` | Request terkirim. Idealnya trim spasi atau menolak jika invalid |
| TC-CH2-11 | Setelah bypass: input kosong | Type sudah `text` | 1) Kosongkan field 2) Submit | (kosong) | Jika wajib, sistem menolak (server-side). Dicatat hasilnya |
| TC-CH2-12 | Setelah bypass: angka negatif | Type sudah `text` | 1) Isi angka negatif 2) Submit | `-10` | Request terkirim. Jika hanya positif, idealnya ditolak |
| TC-CH2-13 | Setelah bypass: angka sangat besar | Type sudah `text` | 1) Isi angka sangat besar 2) Submit | `99999999999999999999` | Sistem stabil. Jika ada limit, muncul pesan error yang jelas |
| TC-CH2-14 | Bypass tambahan: hapus min/max/step (jika ada) | DevTools terbuka, field punya atribut min/max/step | 1) Inspect field 2) Hapus min/max/step 3) Isi out of range 4) Submit | contoh `99999` | Validasi client-side bisa dilewati, request terkirim, respon dicatat |

---

# Lampiran – Bukti Pengerjaan Testing Challenges

> Catatan: supaya gambar muncul di file Markdown, simpan screenshot di folder yang sama dengan file `.md` ini.  
> Nama file yang disarankan:
> - `bukti_challenge1.png` (untuk Challenge #1)
> - `bukti_challenge2.png` (untuk Challenge #2)

## A. Bukti Challenge #1 – Web Testing
**Link:** http://testingchallenges.thetestingmap.org/  
**Fokus:** field **First Name** (max length 30).

### A.1 Screenshot
![Bukti Challenge #1](bukti_challenge1.png)

### A.2 Ringkasan yang saya lakukan
Di Challenge #1, saya melakukan pengujian variasi input pada field First Name untuk memenuhi checklist yang ada di halaman, seperti:
- empty value dan spasi,
- spasi di awal/akhir/tengah,
- input non-alfabet, non-ASCII,
- uji HTML tags, basic XSS, basic SQL injection,
- boundary value berdasarkan panjang input (minimum, average, maximum 30, dan >30),
- aktivitas tambahan sesuai challenge: melihat page source, melihat cookie, dan uji missing CSS, serta mencoba mengubah role user menjadi admin lewat cookie/storage (jika parameter tersedia).

---

## B. Bukti Challenge #2 – Bypass HTML5 Validations
**Link:** http://testingchallenges.thetestingmap.org/challenge2.php  

### B.1 Screenshot
![Bukti Challenge #2](bukti_challenge2.png)

### B.2 Ringkasan langkah bypass yang saya lakukan
1. Saya membuka **DevTools** dengan menekan **F12**.  
2. Saya melakukan **Inspect Element** pada field input angka (yang divalidasi HTML5).  
3. Pada tab **Elements**, saya ubah atribut input dari:
   - `type="number"`  
   menjadi:
   - `type="text"`  
4. Setelah diubah menjadi text, saya mencoba memasukkan data non-integer (huruf/simbol/desimal) agar terbukti validasi HTML5 bisa dilewati.

### B.3 Kesimpulan singkat
Validasi HTML5 sifatnya client-side, jadi bisa dimanipulasi lewat DevTools. Karena itu, seharusnya sistem tetap punya validasi server-side supaya data yang masuk tetap benar dan tidak mudah dimanipulasi.

---

# Penutup (Singkat)
Dari hasil analisis McCall, kualitas sistem SIAKAD secara keseluruhan masih **Cukup** dan mendekati batas **Baik**, tetapi faktor yang paling perlu perhatian adalah **Maintainability**, diikuti **Interoperability**. Sementara dari testing challenge, saya dapat pelajaran bahwa pengujian input dan validasi itu penting, dan validasi client-side (HTML5) tetap harus diperkuat dengan validasi di server.
