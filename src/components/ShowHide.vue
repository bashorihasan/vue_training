<template>
  <section class="card">
    <h2>Show/Hide Content</h2>
    <button @click="toggleContent" class="btn btn-info">
      {{ showContent ? 'Sembunyikan' : 'Tampilkan' }} Konten
    </button>
    <div v-show="showContent" class="content-box">
      <p>Ini adalah konten yang bisa ditampilkan atau disembunyikan menggunakan Vue.js!</p>
      <p>Vue.js membuat reactive programming menjadi mudah dan menyenangkan.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ShowHide',
  data() {
    return {
      showContent: false
    }
  },
  methods: {
    toggleContent() {
      this.showContent = !this.showContent
    }
  }
}
</script>

<style scoped>
.card {
  background: white;
  border-radius: 15px;
  padding: 30px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
}

.card h2 {
  color: #667eea;
  margin-bottom: 20px;
  font-size: 1.8em;
  border-bottom: 3px solid #667eea;
  padding-bottom: 10px;
}

.btn {
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 1em;
  font-weight: 600;
  transition: all 0.3s ease;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.btn:hover {
  transform: scale(1.05);
}

.btn-info {
  background: #4299e1;
  color: white;
}

.content-box {
  margin-top: 20px;
  padding: 20px;
  background: #edf2f7;
  border-radius: 8px;
  animation: fadeIn 0.5s ease;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.content-box p {
  margin-bottom: 10px;
  line-height: 1.6;
  color: #2d3748;
}
</style>
