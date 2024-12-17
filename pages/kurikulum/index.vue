<template>
  <div class="container-fluid">
    <div class="col-lg-12">
        <h4 style="background-color: black;" class="text-white text-center rounded-3 p-2 m-3">
          Kompetensi Keahlian <b>SMKN 4 TASIKMALAYA</b>
        </h4>
      </div>
      <div class="col-lg-12">
        <p style="background-color: whitesmoke;" class="rounded-3 p-1 m-3 text-secondary">
          <NuxtLink to="/" class="text-decoration-none">Kurikulum</NuxtLink>
        </p>
      </div>
  </div>
  <div class="kompetensi-keahlian">
    <h2>Kompetensi Keahlian</h2>
    <div class="main-card">
      <div class="cards">
        <div 
          class="card" 
          v-for="(kompetensi, index) in kompetensiList" 
          :key="index">
          <div class="icon">
            <i :class="kompetensi.icon"></i>
          </div>
          <div class="content">
            <h3>{{ kompetensi.title }}</h3>
            <ul>
              <li v-for="(sarana, i) in kompetensi.sarana" :key="i">
                {{ sarana }}
              </li>
            </ul>
          </div>
        </div>
      </div>
      <NuxtLink to="kurikulum/Kompetensi-Keahlian">
        <button class="btn">Selengkapnya</button>
      </NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  name: "KompetensiKeahlian",
  setup() {
    const kompetensiList = [
      {
        title: "Teknik Komputer dan Jaringan",
        icon: "fas fa-network-wired",
        sarana: ["Bengkel TKJ", "Network Simulator", "Techno Park", "Dll"]
      },
      {
        title: "Rekayasa Perangkat Lunak",
        icon: "fas fa-code",
        sarana: ["Laboratorium Komputer", "Computer Server", "Techno Park", "Dll"]
      },
      {
        title: "Teknik dan Bisnis Sepeda Motor",
        icon: "fas fa-tools",
        sarana: ["Bengkel TBSM", "Unit Produksi", "Techno Park", "Dll"]
      },
      {
        title: "Teknik Elektronika Industri",
        icon: "fas fa-microchip",
        sarana: ["Lab Elektronika", "Workshop Elektronika", "Techno Park", "Dll"]
      },
      {
        title: "Teknik Konstruksi dan Properti",
        icon: "fas fa-building",
        sarana: ["Studio Gambar", "Lab Material", "Techno Park", "Dll"]
      }
    ];

    return {
      kompetensiList
    };
  }
};
</script>

<style scoped>
.kompetensi-keahlian {
  padding: 20px;
  font-family: 'Roboto', sans-serif;
  background: linear-gradient(to right, #eef2f3, #8e9eab);
  color: #333;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
  font-size: 2rem;
  color: #2c3e50;
  text-transform: uppercase;
}

.main-card {
  background: #ffffff;
  border-radius: 12px;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
  padding: 30px;
  max-width: 1300px;
  margin: 0 auto;
  text-align: center;
}

.cards {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 25px;
}

.card {
  background: #f4f9fc;
  border-radius: 12px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  width: 300px;
  padding: 20px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
}

.icon {
  font-size: 50px;
  margin-bottom: 15px;
  color: #3498db;
}

.content {
  font-size: 16px;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin: 8px 0;
  color: #555;
}

.btn {
  margin-top: 30px;
  padding: 12px 20px;
  background-color: #3498db;
  color: #fff;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.btn:hover {
  background-color: #2980b9;
  transform: translateY(-2px);
}
</style>
