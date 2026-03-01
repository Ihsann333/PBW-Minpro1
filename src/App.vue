<template>
  <div>

    <nav class="nav">
      <h2 class="logo">My Portofolio</h2>
      <ul>
        <li @click="currentPage = 'home'">Home</li>
        <li @click="currentPage = 'about'">About Me</li>
        <li @click="currentPage = 'certificates'">Certificates</li>
      </ul>
    </nav>

    <section v-if="currentPage === 'home'" class="hero">
      <div class="hero-left">
        <p>Hello, I'm</p>
        <h1>Nur Ihsan</h1>
        <h2>Creative Designer & Video Editor</h2>

        <p class="desc">
          Mahasiswa Sistem Informasi yang berfokus pada desain visual kreatif,
          UI/UX website, serta video editing menggunakan perangkat mobile.
        </p>
      </div>

      <div class="hero-right">
        <img src="/Foto.JPG" alt="Foto Ihsan" />
      </div>
    </section>

    <section v-if="currentPage === 'about'" class="about">
      
      <div class="about-left">
        <img src="/Foto.JPG" alt="Foto Ihsan" />
      </div>

      <div class="about-right">
        <h1>About Me</h1>

        <p>
          Saya adalah mahasiswa Sistem Informasi yang memiliki ketertarikan pada 
          desain visual kreatif dan video editing.
        </p>

        <p>
          Saya menikmati proses mengerjakan proyek yang berhubungan dengan desain,
          seperti merancang UI/UX untuk website agar tampil menarik dan mudah digunakan.
        </p>

        <p>
          Dalam bidang video editing, saya menggunakan CapCut dan Alight Motion 
          untuk menghasilkan konten yang lebih maksimal. Seluruh proses editing 
          saya lakukan menggunakan perangkat mobile.
        </p>

<div class="skills">

  <div class="skill-item">
    <div class="skill-header">
      <span>Canva</span>
      <span>90%</span>
    </div>
    <div class="progress">
      <div class="progress-bar" style="width: 90%"></div>
    </div>
    <p class="skill-desc">
      Berpengalaman membuat desain konten media sosial, poster, dan presentasi 
      dengan visual yang menarik dan konsisten.
    </p>
  </div>

  <div class="skill-item">
    <div class="skill-header">
      <span>Figma</span>
      <span>80%</span>
    </div>
    <div class="progress">
      <div class="progress-bar" style="width: 80%"></div>
    </div>
    <p class="skill-desc">
      Mampu merancang UI/UX website mulai dari wireframe hingga prototype 
      interaktif yang user-friendly.
    </p>
  </div>

  <div class="skill-item">
    <div class="skill-header">
      <span>CapCut</span>
      <span>85%</span>
    </div>
    <div class="progress">
      <div class="progress-bar" style="width: 85%"></div>
    </div>
    <p class="skill-desc">
      Mengedit video kreatif untuk konten media sosial dengan transisi, 
      efek, dan sinkronisasi audio yang dinamis.
    </p>
  </div>

  <div class="skill-item">
    <div class="skill-header">
      <span>Alight Motion</span>
      <span>75%</span>
    </div>
    <div class="progress">
      <div class="progress-bar" style="width: 75%"></div>
    </div>
    <p class="skill-desc">
      Membuat animasi teks dan motion graphic sederhana untuk meningkatkan 
      kualitas visual konten video.
    </p>
  </div>
</div>

      </div>

    </section>

    <section v-if="currentPage === 'certificates'" class="section">
      <h1>Certificates</h1>

      <div class="cards">
        <div class="card">
          <img src="/sertifikat1.jpg" alt="Sertifikat 1" />
        </div>

        <div class="card">
          <img src="/sertifikat2.jpg" alt="Sertifikat 2" />
        </div>

        <div class="card">
          <img src="/sertifikat3.jpg" alt="Sertifikat 3" />
        </div>
      </div>
    </section>

  </div>
</template>

<script>
export default {
  data() {
    return {
      currentPage: "home"
    }
  }
}
</script>

<style scoped>

.hero{
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:100px 80px;
  min-height:80vh;
  background: linear-gradient(135deg,#ff5f1f,#5b0000);
  border-radius:40px;
  margin:40px;
}

.hero-left{
  max-width:500px;
}

.hero h1{
  font-size:70px;
  margin:10px 0;
}

.hero h2{
  font-size:28px;
  font-weight:300;
}

.hero-right img{
  width:350px;
  border-radius:30px;
  box-shadow:0 20px 40px rgba(0,0,0,0.5);
}

.about{
  display:flex;
  align-items:center;
  gap:60px;
  padding:100px 80px;
  background:#0c0c0c;
  border-radius:40px;
  margin:40px;
}

.about-left img{
  width:300px;
  border-radius:30px;
}

.about-right{
  max-width:600px;
}

.skills{
  margin-top:20px;
  display:flex;
  gap:15px;
  flex-wrap:wrap;
}

.skills span{
  background:#ff5f1f;
  padding:8px 15px;
  border-radius:20px;
  font-size:14px;
}

.card img{
  width:100%;
  height:100%;
  object-fit:cover;
  border-radius:20px;
}

</style>