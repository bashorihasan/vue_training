<template>
  <section class="card">
    <h2>Counter App</h2>
    <div class="counter">
      <button @click="decrement" class="btn btn-danger">-</button>
      <span class="counter-value">{{ counter }}</span>
      <button @click="increment" class="btn btn-success">+</button>
    </div>
    <button @click="resetCounter" class="btn btn-secondary">Reset</button>
  </section>
</template>

<script>
export default {
  name: 'CounterApp',
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    increment() {
      this.counter++
    },
    decrement() {
      this.counter--
    },
    resetCounter() {
      this.counter = 0
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

.counter {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  margin: 25px 0;
}

.counter-value {
  font-size: 3em;
  font-weight: bold;
  color: #667eea;
  min-width: 80px;
  text-align: center;
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

.btn-success {
  background: #48bb78;
  color: white;
  font-size: 1.5em;
  width: 50px;
  height: 50px;
  border-radius: 50%;
}

.btn-danger {
  background: #f56565;
  color: white;
  font-size: 1.5em;
  width: 50px;
  height: 50px;
  border-radius: 50%;
}

.btn-secondary {
  background: #718096;
  color: white;
}

@media (max-width: 768px) {
  .counter-value {
    font-size: 2em;
  }
}
</style>
