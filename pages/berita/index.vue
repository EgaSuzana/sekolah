<template>
  <div id="app">
    <div class="container-fluid">
      <div class="row">

        <!-- Berita Terbaru -->
        <div class="col-md-6">
          <div class="card">
            <div class="card-header bg-primary text-white">
              <h5>Berita</h5>
            </div>
            <div class="card-body">
              <div v-for="(berita, index) in beritaList" :key="index" class="berita-item">
                <div class="d-flex">
                  <img :src="berita.icon" alt="Icon" class="icon mr-3">
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
        <div class="col-md-6">
          <div class="card">
            <div class="card-header bg-danger text-white">
              <h5>Pengumuman Terbaru</h5>
            </div>
            <div class="card-body">
              <div v-for="(pengumuman, index) in pengumumanList" :key="index" class="pengumuman-item">
                <div class="d-flex">
                  <img :src="pengumuman.icon" alt="Icon" class="icon mr-3">
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
        {
          icon: "path/to/icon-ppdb.png",
          judul: "Hasil Seleksi PPDB Tahap 2 Tahun 2020",
          tanggal: "08-07-2020",
          sumber: "Taufik Hidayat",
        },
        // Tambahkan data lainnya...
      ],
      pengumumanList: [
        {
          icon: "path/to/icon-un.png",
          judul: "Konfirmasi Kunjungan Industri 2020",
          tanggal: "03-01-2020",
          sumber: "Kepada Siswa",
        },
        {
          icon: "path/to/icon-un.png",
          judul: "Hasil Gladi Bersih UNBK 2020",
          tanggal: "22-01-2020",
          sumber: "",
        },
        // Tambahkan data lainnya...
      ],
      fotoBeritaList: [
        {
          gambar: "path/to/foto1.jpg",
          judul: "Kegiatan Upacara Bendera",
          deskripsi: "Siswa-siswi mengikuti upacara bendera dengan khidmat.",
        },
        {
          gambar: "path/to/foto2.jpg",
          judul: "Lomba Kebersihan Kelas",
          deskripsi: "Para siswa bersemangat mengikuti lomba kebersihan kelas.",
        },
        {
          gambar: "path/to/foto3.jpg",
          judul: "Pentas Seni Sekolah",
          deskripsi: "Penampilan tari tradisional dalam acara pentas seni.",
        },
      ],
    };
  },
};
</script>

<style scoped>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background-color: #f9f9f9;
}

.container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  padding: 20px;
}

/* Slider */
.slider {
  flex: 3;
  position: relative;
  background-color: #fff;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  overflow: hidden;
}

.slider-content {
  padding: 20px;
  text-align: center;
}

.slider-content h2 {
  font-size: 18px;
  background-color: rgba(0, 0, 0, 0.7);
  color: #fff;
  padding: 10px;
  border-radius: 5px;
}

.slider-content p {
  margin: 10px 0;
  font-size: 14px;
  color: #555;
}

.slider-image {
  width: 100%;
  height: auto;
  margin: 10px 0;
}

.slider-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.btn-berita {
  background-color: #007bff;
  color: #fff;
  padding: 8px 15px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.btn-berita:hover {
  background-color: #0056b3;
}
</style>