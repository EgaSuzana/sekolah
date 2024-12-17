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
      <div class="col-md-6 p-5">
        <div class="card">
          <div class="card-header bg-primary text-white">
            <h5>Berita</h5>
          </div>
          <div class="card-body">
            <div v-for="(berita, index) in beritaList" :key="index" class="berita-item">
              <div class="d-flex">
                <img :src="berita.icon" alt="Icon" class="icon mr-3" />
                <div>
                  <h6 class="text-danger">{{ berita.judul }}</h6>
                  <p class="mb-1 text-muted">{{ berita.tanggal }} - {{ berita.sumber }}</p>
                </div>
              </div>
              <hr v-if="index < beritaList.length - 1" />
            </div>
          </div>
          <div class="card-footer text-center">
            <button class="btn btn-primary">Indeks Berita</button>
          </div>
        </div>
      </div>

      <!-- Pengumuman Terbaru -->
      <div class="col-md-6 p-5">
        <div class="card">
          <div class="card-header bg-danger text-white">
            <h5>Pengumuman Terbaru</h5>
          </div>
          <div class="card-body">
            <div v-for="(pengumuman, index) in pengumumanList" :key="index" class="pengumuman-item">
              <div class="d-flex">
                <img :src="pengumuman.icon" alt="Icon" class="icon mr-3" />
                <div>
                  <h6>{{ pengumuman.judul }}</h6>
                  <p class="mb-1 text-muted">{{ pengumuman.tanggal }} - {{ pengumuman.sumber }}</p>
                </div>
              </div>
              <hr v-if="index < pengumumanList.length - 1" />
            </div>
          </div>
          <div class="card-footer text-center">
            <button class="btn btn-danger">Indeks Pengumuman</button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Kompetensi Keahlian -->
  <div class="kompetensi-container">
    <div class="header">
      <h2>📚 Kompetensi Keahlian</h2>
    </div>
    <div class="grid-container">
      <div class="kompetensi-card" v-for="(item, index) in kompetensiList" :key="index">
        <div class="icon">
          <img :src="item.icon" alt="icon" />
        </div>
        <div class="content">
          <h3>{{ item.title }}</h3>
          <strong>Sarana pendukung pembelajaran:</strong>
          <ul>
            <!-- Menampilkan semua sarana -->
            <li v-for="(sarana, i) in item.sarana" :key="i">{{ sarana }}</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      beritaList: [
        {
          icon: "logo.png",
          judul: "Pengumuman Kelulusan Siswa Tahun Pelajaran 2023/2024",
          tanggal: "06-06-2024",
          sumber: "SMKN 4 Tasikmalaya",
        },
      ],
      pengumumanList: [
        {
          icon: "path/to/icon-un.png",
          judul: "Konfirmasi Kunjungan Industri 2020",
          tanggal: "03-01-2020",
          sumber: "Kepada Siswa",
        },
      ],
      kompetensiList: [
        {
          title: "Teknik Komputer dan Jaringan",
          sarana: ["Bengkel TKJ", "Network Simulator", "Techno Park", "Dll"],
          icon: "https://cdn-icons-png.flaticon.com/512/1828/1828778.png",
        },
        {
          title: "Rekayasa Perangkat Lunak",
          sarana: ["Laboratorium Komputer", "Computer Server", "Techno Park", "Dll"],
          icon: "https://cdn-icons-png.flaticon.com/512/1828/1828765.png",
        },
        {
          title: "Teknik dan Bisnis Sepeda Motor",
          sarana: ["Bengkel TBSM", "Unit Produksi", "Techno Park", "Dll"],
          icon: "https://cdn-icons-png.flaticon.com/512/1828/1828843.png",
        },
        {
          title: "Desain Komunikasi Visual",
          sarana: ["Bengkel DKV", "Unit Produksi", "Techno Park", "Dll"],
          icon: "https://cdn-icons-png.flaticon.com/512/1828/1828823.png",
        },
        {
          title: "Teknik Otomasi Industri",
          sarana: ["Bengkel TOI", "Unit Produksi", "Techno Park", "Dll"],
          icon: "https://cdn-icons-png.flaticon.com/512/1828/1828899.png",
        },
      ],
    };
  },
};
</script>

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
  margin: 20px 0;
  background: #f9f9f9;
  border-radius: 8px;
}

.header {
  background-color: #333;
  color: white;
  padding: 15px;
  text-align: center;
  border-radius: 8px 8px 0 0;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  padding: 20px;
}

.kompetensi-card {
  display: flex;
  align-items: flex-start;
  background: white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  padding: 15px;
}

.icon {
  margin-right: 15px;
}

.icon img {
  width: 50px;
  height: 50px;
}

.content h3 {
  margin: 0 0 5px;
  font-size: 1.2rem;
  color: #333;
}

.content strong {
  font-size: 0.9rem;
}

.content ul {
  padding-left: 20px;
  margin: 10px 0 0;
  font-size: 0.9rem;
}

.content ul li {
  margin-bottom: 5px; /* Memberikan jarak antar item */
}
</style>
