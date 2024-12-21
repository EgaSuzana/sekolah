<template>
  <div class="wrapper">
    <!-- Hero Section -->
    <div class="hero">
      <div class="content">
        <h1>SMK NEGERI 4 TASIKMALAYA</h1>
      </div>
    </div>

    <!-- Sambutan Kepala Sekolah -->
    <div class="sambutan">
      <div class="photo">
        <!-- Ganti path dengan lokasi foto kepala sekolah -->
        <img src="" alt="Foto Kepala Sekolah" />
      </div>
      <h2>Sambutan Kepala Sekolah</h2>
      <p>
        Assalamu’alaikum Warahmatullahi Wabarakatuh,  
        Selamat datang di SMK Negeri 4 Tasikmalaya. Kami berkomitmen untuk mencetak generasi unggul, berkarakter, dan siap menghadapi tantangan global.
      </p>
      <p>
        Mari bersama-sama membangun prestasi dan masa depan yang gemilang.
      </p>
      <h4>- Kepala Sekolah</h4>
    </div>
  </div>

  <div class="container-fluid">
    <div class="row">
     <!-- Berita Terbaru -->
     <div class="col-md-6 p-3">
          <div class="card">
            <div class="card-header bg-primary text-white text-center">
              <h5>Berita</h5>
            </div>
            <div class="card-body">
              <div class="berita-item">
                <div class="d-flex">
                  <img src="" alt="Icon" class="icon mr-3">
                  <div>
                    <h6 class="text-danger">Pengumuman Kelulusan Siswa Tahun Pelajaran 2023/2024</h6>
                    <p class="mb-1 text-muted">06-06-2024 - SMKN 4 Tasikmalaya</p>
                  </div>
                </div>
                <hr />
                <div class="d-flex">
                  <img src="" alt="Icon" class="icon mr-3">
                  <div>
                    <h6 class="text-danger">Hasil Seleksi PPDB Tahap 2 Tahun 2020</h6>
                    <p class="mb-1 text-muted">08-07-2020 - Taufik Hidayat</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="card-footer text-center">
              <button class="btn btn-primary">Indeks Berita</button>
            </div>
          </div>
        </div>

        <!-- Pengumuman Terbaru -->
        <div class="col-md-6 p-3">
          <div class="card">
            <div class="card-header bg-danger text-white text-center">
              <h5>Pengumuman Terbaru</h5>
            </div>
            <div class="card-body">
              <div class="pengumuman-item">
                <div class="d-flex">
                  <img src="" alt="Icon" class="icon mr-3">
                  <div>
                    <h6>Konfirmasi Kunjungan Industri 2020</h6>
                    <p class="mb-1 text-muted">03-01-2020 - Kepada Siswa</p>
                  </div>
                </div>
                <hr />
                <div class="d-flex">
                  <img src="" alt="Icon" class="icon mr-3">
                  <div>
                    <h6>Hasil Gladi Bersih UNBK 2020</h6>
                    <p class="mb-1 text-muted">22-01-2020</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="card-footer text-center">
              <button class="btn btn-danger">Indeks Pengumuman</button>
            </div>
          </div>
        </div>
      </div>
  </div>

  <!-- Kompetensi Keahlian Section -->
  <div class="kompetensi-container">
    <div class="header">
      <h2>📚 Kompetensi Keahlian</h2>
    </div>
    <div class="main-card">
      <div class="grid-container">
        <!-- Card 1 -->
        <div class="kompetensi-card">
          <div class="icon">
            <img src="" alt="icon" />
          </div>
          <div class="conten">
            <h3>Teknik Komputer dan Jaringan</h3>
            <strong>Sarana pendukung pembelajaran:</strong>
            <ul>
              <li>Bengkel TKJ</li>
              <li>Network Simulator</li>
              <li>Techno Park</li>
            </ul>
          </div>
        </div>

        <!-- Card 2 -->
        <div class="kompetensi-card">
          <div class="icon">
            <img src="/assets/image/logo pplg.png" alt="icon" />
          </div>
          <div class="conten">
            <h3>Rekayasa Perangkat Lunak</h3>
            <strong>Sarana pendukung pembelajaran:</strong>
            <ul>
              <li>Lab komputer</li>
              <li>Computer Server</li>
              <li>Techno Park</li>
            </ul>
          </div>
        </div>

        <!-- Card 3 -->
        <div class="kompetensi-card">
          <div class="icon">
            <img src="/assets/image/tbsm.png" alt="icon" />
          </div>
          <div class="conten">
            <h3>Teknik Bisnis Sepeda Motor</h3>
            <strong>Sarana pendukung pembelajaran:</strong>
            <ul>
              <li>Studio Editing</li>
              <li>Kamera Profesional</li>
              <li>Lab Animasi</li>
            </ul>
          </div>
        </div>

        <!-- Card 4 -->
        <div class="kompetensi-card">
          <div class="icon">
            <img src="/assets/image/camera.png" alt="icon" />
          </div>
          <div class="conten">
            <h3>Desain Komunikasi Visual</h3>
            <strong>Sarana pendukung pembelajaran:</strong>
            <ul>
              <li>Workshop Elektronika</li>
              <li>Peralatan Soldering</li>
              <li>Lab IoT</li>
            </ul>
          </div>
        </div>

        <!-- Card 5 -->
        <div class="kompetensi-card">
          <div class="icon">
            <img src="/assets/image/toi.png" alt="icon" />
          </div>
          <div class="conten">
            <h3>Teknik Otomasi Industri</h3>
            <strong>Sarana pendukung pembelajaran:</strong>
            <ul>
              <li>Bengkel Mesin</li>
              <li>Simulator CNC</li>
              <li>Peralatan Las</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="footer">
        <button class="btn btn-primary">Selengkapnya</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Wrapper untuk Hero dan Sambutan */
.wrapper {
  display: flex;
  width: 100%;
  height: 80vh;
}

/* Hero Section */
.hero {
  flex: 4; /* Membagi area hero */
  position: relative;
  background: url('') no-repeat center center/cover;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
}

.hero::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5); /* Overlay gelap */
  z-index: 1;
}

.content {
  position: relative;
  z-index: 2;
  color: #fff;
  padding: 20px;
}

h1 {
  font-size: 3rem;
  color: #ffcc00; /* Warna kuning */
  margin: 10px 0;
}

/* Sambutan Kepala Sekolah */
.sambutan {
  flex: 1; /* Membagi area untuk sambutan */
  display: flex;
  flex-direction: column;
  align-items: center; /* Tengah secara horizontal */
  justify-content: center;
  padding: 2rem;
  background-color: #f9f9f9; /* Warna latar abu muda */
  color: #333;
}

.sambutan .photo img {
  width: 150px; /* Ukuran foto kepala sekolah */
  height: 150px;
  border-radius: 50%; /* Membuat foto menjadi bulat */
  object-fit: cover;
  margin-bottom: 1rem;
  border: 3px solid #ffcc00; /* Bingkai foto berwarna kuning */
}

.sambutan h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
  text-align: center;
}

.sambutan p {
  font-size: 1rem;
  line-height: 1.5;
  margin-bottom: 1rem;
  text-align: center;
}

.sambutan h4 {
  font-size: 1.1rem;
  text-align: right;
  margin-top: 1rem;
  color: #555;
}

/* Kompetensi Keahlian */
.kompetensi-container {
  font-family: Arial, sans-serif;
  padding: 20px;
  background: linear-gradient(135deg, #f5f7fa, #c3cfe2);
}

.header h2 {
  text-align: center;
  margin-bottom: 20px;
  color: #333;
  font-size: 2em;
}

.main-card {
  border: 2px solid #ccc;
  border-radius: 12px;
  padding: 20px;
  background: #fff;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 20px;
  justify-items: center;
  align-items: start;
}

.kompetensi-card {
  border: none;
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  background: linear-gradient(135deg, #ffffff, #e6e9f0);
  text-align: center;
  transition: transform 0.3s, box-shadow 0.3s;
}

.kompetensi-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
}

.kompetensi-card .icon img {
  width: 50px;
  height: 50px;
  margin-bottom: 15px;
  border-radius: 50%;
  border: 2px solid #ddd;
}

.kompetensi-card .conten h3 {
  font-size: 1.4em;
  margin: 15px 0;
  color: #333;
}

.kompetensi-card ul {
  list-style: none;
  padding: 0;
  text-align: left;
}

.kompetensi-card ul li {
  margin: 5px 0;
  color: #555;
}

.footer {
  text-align: center;
  margin-top: 20px;
}

.footer .btn {
  background-color: #007bff;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 1em;
}

.footer .btn:hover {
  background-color: #0056b3;
}
</style>
