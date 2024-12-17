<template>
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
            <li v-for="(sarana, i) in item.sarana" :key="i">{{ sarana }}</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      kompetensiList: [
        {
          title: "Teknik Komputer dan Jaringan",
          sarana: ["Bengkel TKJ", "Network Simulator", "Techno Park", "Dll"],
          icon: "https://cdn-icons-png.flaticon.com/512/1828/1828778.png", // Replace with proper icon path
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
.kompetensi-container {
  margin: 20px;
}

.header {
  background-color: #333;
  color: white;
  padding: 15px;
  text-align: center;
  border-radius: 8px 8px 0 0;
}

.header h2 {
  margin: 0;
  font-size: 1.5rem;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  padding: 20px;
  background: #f9f9f9;
  border-radius: 0 0 8px 8px;
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

.content li {
  margin-bottom: 5px;
}
</style>
