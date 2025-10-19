<template>
  <section id="about" class="about">
    <div class="container">
      <div class="section-header">
        <h2>About Us</h2>
        <p>Learn more about our company and mission</p>
      </div>
      <div class="about-content">
        <div class="about-text">
          <h3>{{ heading }}</h3>
          <p>{{ description }}</p>
          <div class="stats">
            <div class="stat-item" v-for="stat in stats" :key="stat.label">
              <h4>{{ stat.value }}</h4>
              <p>{{ stat.label }}</p>
            </div>
          </div>
        </div>
        <div class="about-image">
          <div class="image-placeholder">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
            </svg>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About',
  data() {
    return {
      heading: 'Building the Future of Technology',
      description: 'TechVision is a leading technology company dedicated to delivering innovative solutions that drive business growth. With over 10 years of experience, we have helped hundreds of clients transform their digital presence and achieve their goals. Our team of experts combines creativity with technical expertise to deliver exceptional results.',
      stats: [
        { value: '10+', label: 'Years Experience' },
        { value: '500+', label: 'Projects Completed' },
        { value: '200+', label: 'Happy Clients' },
        { value: '50+', label: 'Team Members' }
      ]
    }
  }
}
</script>

<style scoped>
.about {
  background: #f8f9fa;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.section-header {
  text-align: center;
  margin-bottom: 60px;
}

.section-header h2 {
  font-size: 2.5em;
  color: #2c3e50;
  margin-bottom: 10px;
}

.section-header p {
  color: #7f8c8d;
  font-size: 1.1em;
}

.about-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}

.about-text h3 {
  font-size: 2em;
  color: #2c3e50;
  margin-bottom: 20px;
}

.about-text p {
  color: #555;
  font-size: 1.1em;
  line-height: 1.8;
  margin-bottom: 30px;
}

.stats {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
}

.stat-item {
  text-align: center;
  padding: 20px;
  background: white;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.stat-item:hover {
  transform: translateY(-5px);
}

.stat-item h4 {
  font-size: 2.5em;
  color: #667eea;
  margin-bottom: 5px;
}

.stat-item p {
  color: #7f8c8d;
  font-size: 0.9em;
  margin: 0;
}

.about-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-placeholder {
  width: 100%;
  height: 400px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.image-placeholder svg {
  width: 150px;
  height: 150px;
  color: white;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .about-content {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .stats {
    grid-template-columns: 1fr;
  }

  .section-header h2 {
    font-size: 2em;
  }

  .about-text h3 {
    font-size: 1.5em;
  }
}
</style>
