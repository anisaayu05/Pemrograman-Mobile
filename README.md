# HireMe - Aplikasi Pencarian Pekerjaan

## Deskripsi Proyek

Proyek ini adalah bagian dari mata kuliah Pemrograman Mobile untuk mengajarkan pengembangan aplikasi mobile dengan **Flutter**. Fokus utama mencakup **navigasi**, **state management**, dan **akses data**.

### Tautan Prototipe Figma
Untuk melihat prototipe aplikasi HireMe, silakan kunjungi: [Figma Prototype](https://www.figma.com/design/bCdjLRwIq7X6V5IIX8K3rW/HireMe-App?node-id=0-1&t=FbXNFhbINDSmzJEv-1)

### Deskripsi Aplikasi

**HireMe** adalah platform modern yang dirancang untuk membantu pengguna dalam mencari pekerjaan secara efisien. Dengan antarmuka pengguna yang intuitif, aplikasi ini menggunakan Flutter untuk memberikan pengalaman pengguna yang mulus di perangkat mobile. Fokus utama aplikasi ini meliputi:

- **Navigasi Frontend** yang mudah dan jelas
- **Manajemen status** yang efektif
- **Akses data** yang aman
- **Backend yang mudah dikelola admin**

---

## Frontend

Frontend aplikasi **HireMe** berfokus pada pengalaman pengguna, dengan antarmuka yang ramah pengguna dan fitur yang mudah diakses. Berikut adalah beberapa fitur utama dari frontend aplikasi:

### Navigasi
Aplikasi ini memiliki **navigation bar** yang terdiri dari empat tab yang dapat diakses pengguna:

1. **Home** - Halaman utama dengan tombol **Browse Pekerjaan** dan pesan untuk pengguna yang belum terdaftar.
2. **Browse** - Menampilkan daftar pekerjaan dan memungkinkan pengguna melamar pekerjaan setelah login.
3. **Applied** - Menampilkan daftar pekerjaan yang sudah dilamar dan status lamaran.
4. **Profile** - Menampilkan dan memungkinkan pengguna mengedit informasi profil seperti nama, email, dan foto profil.

### Halaman dan Fungsionalitas

#### 1. Home
- **Fitur Utama**: Menampilkan tombol **Browse Pekerjaan** yang mengarahkan pengguna ke halaman **Browse**.
- **Informasi**: Keterangan tentang berbagai situs pencarian pekerjaan, termasuk **LinkedIn**.
- **Pengguna Belum Mendaftar**: Menampilkan pesan yang mendorong pengguna untuk **Create Akun** agar dapat mengakses semua fitur aplikasi.
- **Desain UI**: Desain antarmuka yang menarik secara visual dengan warna cerah dan elemen yang jelas.

#### 2. Browse
- **Pengguna Belum Login**: Masih dapat melihat daftar pekerjaan, tetapi tidak dapat melihat rincian atau melamar pekerjaan.
- **Pengguna Setelah Login**: Memiliki akses penuh ke rincian pekerjaan, termasuk:
  - **Judul Pekerjaan**
  - **Deskripsi Pekerjaan**
  - **Persyaratan**
  - **Deskripsi Perusahaan**
  - **Tombol Lamaran** untuk memulai proses aplikasi.

##### **Proses Melamar Pekerjaan**
- **Mengisi Formulir Lamaran**: Pengguna mengisi informasi pribadi, pengalaman kerja, dan pendidikan.
- **Upload CV**: CV diunggah dalam format PDF atau DOCX dengan instruksi yang jelas.
- **Konfirmasi Lamaran**: Pengguna menerima konfirmasi setelah melamar.

#### 3. Applied
- **Pengguna Belum Login**: Halaman tidak dapat diakses.
- **Pengguna Setelah Login**: Dapat melihat daftar pekerjaan yang telah dilamar dan status setiap lamaran:
  - **Status Lamaran**: Menampilkan status apakah dalam proses, diterima, atau ditolak.
  - **Riwayat Lamaran**: Melihat waktu dan tanggal lamaran, serta opsi untuk mengulangi atau membatalkan lamaran.
- **Desain yang Intuitif**: Tabel atau daftar yang jelas untuk menampilkan informasi.

#### 4. Profile
- **Pengguna Belum Login**: Tidak dapat mengakses halaman.
- **Pengguna Setelah Login**: Dapat memperbarui informasi akun seperti nama, email, foto profil, dan preferensi pencarian pekerjaan.
- **Riwayat dan Notifikasi**: Melihat notifikasi terkait lamaran dan pembaruan dari perusahaan.

### Verifikasi Dua Langkah (OTP)

Fitur keamanan tambahan yang membantu melindungi akun pengguna.

- **Tujuan OTP**: Mengurangi risiko pencurian identitas dengan memastikan hanya pengguna sah yang dapat mengakses akun.
- **Implementasi**:
  - OTP dikirim melalui **SMS** atau **email** setelah login.
  - Pengguna dapat memilih metode pengiriman OTP saat membuat akun.
- **Manfaat**: Pengguna merasa lebih aman dan memiliki kontrol lebih besar atas akses ke akun.

### Kesimpulan Frontend

Aplikasi **HireMe** dirancang untuk memberikan pengalaman pencarian pekerjaan yang **efektif** dan **aman** bagi pengguna melalui antarmuka yang intuitif. Dengan **navigasi frontend** yang jelas, pengguna dapat dengan mudah berpindah antara halaman-halaman penting aplikasi, seperti **Home**, **Browse**, **Applied**, dan **Profile**. Desain yang ramah pengguna serta fitur seperti formulir lamaran pekerjaan dan manajemen profil menjadikan aplikasi ini mudah digunakan. Sistem keamanan dua langkah (OTP) juga memastikan aplikasi ini aman digunakan.

---

## Backend

Backend aplikasi **HireMe** fokus pada pengelolaan data terkait pekerjaan, kandidat, dan perusahaan. Admin dapat mengelola informasi penting dan statistik yang membantu dalam pengambilan keputusan serta pengelolaan aplikasi.

### Navigasi Backend
Backend admin HireMe memiliki empat bagian utama yang diakses melalui navigation bar di bagian bawah:

1. **Dashboard**: Untuk menampilkan statistik utama, aktivitas terkini, pengumuman, dan jadwal.
2. **Company**: Untuk mengelola informasi perusahaan, seperti data karyawan dan pengumuman internal.
3. **Candidate**: Untuk melihat daftar kandidat, riwayat lamaran, dan status seleksi.
4. **Profile**: Mengelola informasi akun admin dan pengaturan notifikasi.

### Halaman Dashboard Admin dan Fitur Utama

#### 1. Dashboard
Halaman Dashboard adalah pusat kontrol admin, menampilkan informasi kunci seperti statistik dan aktivitas yang berlangsung di platform:

- **Search Bar**: Memungkinkan admin mencari informasi tertentu dengan cepat, misalnya nama karyawan, kandidat, atau posisi pekerjaan.
  
#### Statistik Utama:
- **Total Employees**: Menampilkan jumlah total karyawan yang terdaftar di platform, dibagi menurut gender (laki-laki dan perempuan).
- **Job View**: Menunjukkan jumlah total tampilan pada semua lowongan pekerjaan, dilengkapi dengan persentase perubahan dari periode sebelumnya.
- **Job Applied**: Menampilkan jumlah total lamaran pekerjaan yang masuk, termasuk detail menurut gender kandidat.
- **Resigned Employees**: Memberikan informasi tentang jumlah karyawan yang sudah mengundurkan diri, dengan persentase perubahan yang membantu admin melacak tren pengunduran diri.

#### Pengumuman (Announcement):
- Menampilkan pengumuman penting seperti jadwal outing, pertemuan departemen, atau kebutuhan posisi baru di perusahaan.

#### Aktivitas Terbaru (Recently Activity):
- Menunjukkan aktivitas yang baru saja dilakukan oleh admin atau tim HR, seperti memposting pekerjaan baru atau memperbarui status lamaran.

#### Jadwal Mendatang (Upcoming Schedule):
- Menyediakan informasi tentang jadwal penting yang akan datang, termasuk review aplikasi kandidat dan jadwal wawancara.

#### 2. Company
Halaman **Company** digunakan untuk melihat dan mengelola data terkait perusahaan, seperti daftar karyawan dan informasi departemen. Admin dapat menambah atau memperbarui pengumuman internal serta meninjau statistik karyawan di setiap departemen.

#### 3. Candidate
Di halaman **Candidate**, admin dapat melihat semua kandidat yang telah mendaftar untuk posisi yang ada, termasuk data lamaran, CV yang diunggah, dan status seleksi. Fitur ini membantu admin melacak proses rekrutmen dan melakukan tindakan lebih lanjut, seperti menjadwalkan wawancara atau mengirim notifikasi.

#### 4. Profile
Halaman **Profile** memungkinkan admin memperbarui informasi akun mereka, termasuk nama, email, dan preferensi notifikasi. Admin juga dapat mengatur pengaturan keamanan akun untuk menjaga data tetap aman.

### Kesimpulan Backend

Bagian backend **HireMe** menyediakan alat yang lengkap dan mudah digunakan bagi administrator untuk mengelola dan memantau aktivitas di platform pencarian pekerjaan. Dengan fitur statistik, manajemen kandidat, pengumuman, dan jadwal yang terintegrasi, admin dapat memastikan platform berjalan secara efektif dan efisien untuk mendukung pengalaman pencarian pekerjaan yang lebih baik bagi pengguna.

---

## Kesimpulan Aplikasi HireMe

Aplikasi **HireMe** secara keseluruhan menyediakan solusi pencarian pekerjaan yang terintegrasi antara frontend dan backend. Pengguna dapat dengan mudah mencari dan melamar pekerjaan melalui antarmuka yang ramah pengguna, sementara admin memiliki alat yang kuat untuk mengelola data dan memantau aktivitas di platform. Fitur keamanan seperti verifikasi dua langkah (OTP) memastikan bahwa aplikasi ini aman bagi semua penggunanya. Dengan manajemen data yang efisien di sisi backend dan pengalaman pengguna yang optimal di sisi frontend, aplikasi **HireMe** siap menjadi platform pencarian pekerjaan yang efektif dan aman.
