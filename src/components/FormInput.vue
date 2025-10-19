<template>
  <section class="card">
    <h2>Form Input</h2>
    <form @submit.prevent="handleSubmit">
      <div class="form-group">
        <label>Nama:</label>
        <input v-model="formData.name" type="text" required>
      </div>
      <div class="form-group">
        <label>Email:</label>
        <input v-model="formData.email" type="email" required>
      </div>
      <div class="form-group">
        <label>Pesan:</label>
        <textarea v-model="formData.message" rows="4" required></textarea>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
    <div v-if="submittedData" class="result">
      <h3>Data yang Disubmit:</h3>
      <p><strong>Nama:</strong> {{ submittedData.name }}</p>
      <p><strong>Email:</strong> {{ submittedData.email }}</p>
      <p><strong>Pesan:</strong> {{ submittedData.message }}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FormInput',
  data() {
    return {
      formData: {
        name: '',
        email: '',
        message: ''
      },
      submittedData: null
    }
  },
  methods: {
    handleSubmit() {
      this.submittedData = { ...this.formData }
      alert('Form berhasil disubmit! Lihat data di bawah form.')
      // Reset form
      this.formData = {
        name: '',
        email: '',
        message: ''
      }
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

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 8px;
  color: #2d3748;
  font-weight: 600;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 12px;
  border: 2px solid #e2e8f0;
  border-radius: 8px;
  font-size: 1em;
  font-family: inherit;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #667eea;
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

.btn-primary {
  background: #667eea;
  color: white;
}

.btn-primary:hover {
  background: #5568d3;
}

.result {
  margin-top: 25px;
  padding: 20px;
  background: #f0fff4;
  border-left: 4px solid #48bb78;
  border-radius: 8px;
}

.result h3 {
  color: #38a169;
  margin-bottom: 15px;
}

.result p {
  margin-bottom: 10px;
  color: #2d3748;
}
</style>
