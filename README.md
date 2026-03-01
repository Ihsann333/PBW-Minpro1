## Nur Ihsan
## 2409116051

## Tampilan Setiap Section / Fitur


<img width="1919" height="979" alt="image" src="https://github.com/user-attachments/assets/3c1960be-df96-4c1c-b21f-6bebbaf26282" />

**1. Navbar (Navigasi)**

Tampilan:

* Terletak di bagian atas halaman.

* Berisi teks “My Portofolio”.

* Menu navigasi: Home, About Me, Certificates. Saat diklik, halaman berubah tanpa reload.

Fitur:

* Menggunakan event @click

* Mengubah nilai currentPage

* Menggunakan v-if untuk menampilkan section sesuai halaman aktif


<img width="1919" height="979" alt="image" src="https://github.com/user-attachments/assets/5733d98a-8e0e-4a9c-9e03-891d0dace10b" />

**2. Section Home**

Tampilan:

Background gradasi warna merah-oranye.

Di kiri:

* Nama: Nur Ihsan

* Profesi: Creative Designer & Video Editor

* Deskripsi singkat

Di kanan:

* Foto pribadi

* Layout menggunakan Flexbox (kiri dan kanan sejajar)


<img width="1917" height="983" alt="image" src="https://github.com/user-attachments/assets/e2a9c42f-e98f-4ff1-9a96-abf176cbf168" />

**3. Section About Me**

Tampilan:

* Background warna gelap (#0c0c0c)

Layout 2 kolom:

* Kiri: Foto

* Kanan: Paragraf deskripsi

* Di bawah deskripsi ada skill tags


<img width="1912" height="978" alt="image" src="https://github.com/user-attachments/assets/29b500a5-abdc-4839-9852-af6893123c59" />

**4. Section Certificates**

Tampilan:

* Background lebih gelap

* Judul “Certificates”

* 3 sertifikat berjajar

* Setiap card berisi gambar sertifikat

## Penjelasan Code Setiap Section/Fitur

**1. Navbar**

<nav class="nav">
  <h2 class="logo">My Portofolio</h2>
  <ul>
    <li @click="currentPage = 'home'">Home</li>
    <li @click="currentPage = 'about'">About Me</li>
    <li @click="currentPage = 'certificates'">Certificates</li>
  </ul>
</nav>

Navbar berfungsi sebagai elemen navigasi utama pada website portfolio. <nav> digunakan untuk membungkus seluruh menu navigasi, sementara <h2 class="logo"> menampilkan judul website. Menu navigasi dibuat menggunakan <ul> dan <li> agar terstruktur. Setiap item menu memiliki @click yang terhubung dengan Vue.js untuk mengubah nilai variabel currentPage. Ketika salah satu menu diklik, nilai currentPage akan berubah sesuai halaman yang dipilih, sehingga secara otomatis memperbarui tampilan tanpa perlu melakukan reload halaman.

**2. Sistem Navigasi**

export default {
  data() {
    return {
      currentPage: "home"
    }
  }
}

Sistem navigasi pada website ini menggunakan state management sederhana dengan properti data() pada Vue.js. Variabel currentPage didefinisikan, berfungsi untuk menyimpan informasi halaman yang sedang aktif. Nilai awal currentPage diset ke "home", sehingga ketika website pertama kali dibuka, halaman Home langsung ditampilkan. Setiap perubahan nilai currentPage akan langsung dideteksi oleh sistem Vue, sehingga tampilan halaman dapat berubah secara dinamis sesuai kondisi yang ditentukan.

**3. Home Section**

<section v-if="currentPage === 'home'" class="hero">

<div class="hero-left">

<div class="hero-right">
  <img src="/Foto.JPG" />
</div>

.hero{
  display:flex;
  justify-content:space-between;
  align-items:center;
}



Home section ditampilkan menggunakan v-if dengan kondisi currentPage'home'. Artinya section ini hanya akan dirender ketika halaman Home sedang aktif. Di dalam home section, layout dibagi menjadi dua bagian, yaitu sisi kiri untuk teks perkenalan dan sisi kanan untuk menampilkan gambar profil. Pengaturan tata letak menggunakan Flexbox dengan display: flex, sehingga konten dapat disejajarkan secara horizontal dan terlihat rapi di berbagai ukuran layar.

**4. About Section**

<section v-if="currentPage === 'about'" class="about">

<div class="about-left">

<div class="about-left">

<div class="skills">
  <span>Canva</span>
</div>

.skills{
  display:flex;
  gap:15px;
  flex-wrap:wrap;
}

About section juga menggunakan directive v-if dengan kondisi currentPage 'about', jadi hanya muncul ketika menu about dipilih. Struktur section ini dibagi menjadi dua bagian utama, yaitu bagian kiri untuk menampilkan gambar profil dan bagian kanan untuk menampilkan deskripsi diri serta daftar skill. Skill ditampilkan dalam bentuk tag menggunakan <span> yang dikelompokkan di dalam container .skills. Penggunaan Flexbox dan properti flex-wrap: wrap memungkinkan daftar skill tetap tersusun rapi dan otomatis berpindah ke baris berikutnya ketika ruang layar tidak mencukupi.

**5. Certificates Section**

<section v-if="currentPage === 'certificates'" class="section">

<div class="cards">
  <div class="card">
    <img src="/sertifikat1.jpg" />
  </div>
</div>

.cards{
  display:flex;
  gap:30px;
}

.card img{
  width:100%;
  object-fit:cover;
}

Certificates section berfungsi untuk menampilkan daftar sertifikat yang dimiliki dan hanya akan dirender ketika currentPage bernilai "certificates". Sertifikat ditampilkan dalam bentuk card yang berisi gambar, sehingga tampilan terlihat lebih terstruktur. Container .cards menggunakan Flexbox agar setiap card tersusun secara horizontal dengan jarak yang konsisten. Gambar sertifikat diatur menggunakan properti width: 100% dan object-fit: cover agar gambar menyesuaikan ukuran card tanpa mengalami distorsi atau perubahan proporsi.

**6. Konsep SPA**

Website portfolio ini menerapkan konsep Single Page Application (SPA) sederhana. Seluruh navigasi halaman dikontrol hanya dengan satu variabel state, yaitu currentPage, yang dikombinasikan dengan directive v-if untuk menentukan section mana yang ditampilkan.

## Teknologi yang Digunakan

**1. HTML**

Digunakan untuk:

* Struktur halaman

* Navbar

* Section

* Card sertifikat

* Paragraf & gambar

**2. CSS**

Digunakan untuk:

* Layout (Flexbox)

* Warna background

* Typography

* Border radius

* Box shadow

* Spacing (padding, margin)

**3. Vue.js**

Digunakan untuk:

* Reactive data (data())

* Event handling (@click)

* Conditional rendering (v-if)

* SPA sederhana tanpa reload
