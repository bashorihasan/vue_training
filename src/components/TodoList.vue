<template>
  <section class="card">
    <h2>Todo List</h2>
    <div class="todo-input">
      <input 
        v-model="newTodo" 
        @keyup.enter="addTodo"
        type="text" 
        placeholder="Tambahkan todo baru..."
      >
      <button @click="addTodo" class="btn btn-primary">Tambah</button>
    </div>
    <ul class="todo-list">
      <li v-for="(todo, index) in todos" :key="index" :class="{ completed: todo.completed }">
        <input 
          type="checkbox" 
          v-model="todo.completed"
        >
        <span>{{ todo.text }}</span>
        <button @click="removeTodo(index)" class="btn-remove">×</button>
      </li>
    </ul>
    <p v-if="todos.length === 0" class="empty-message">Belum ada todo. Silakan tambahkan!</p>
  </section>
</template>

<script>
export default {
  name: 'TodoList',
  data() {
    return {
      newTodo: '',
      todos: [
        { text: 'Belajar Vue.js basics', completed: false },
        { text: 'Membuat aplikasi sederhana', completed: false },
        { text: 'Praktek coding setiap hari', completed: false }
      ]
    }
  },
  methods: {
    addTodo() {
      if (this.newTodo.trim()) {
        this.todos.push({
          text: this.newTodo.trim(),
          completed: false
        })
        this.newTodo = ''
      }
    },
    removeTodo(index) {
      this.todos.splice(index, 1)
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

.todo-input {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

.todo-input input {
  flex: 1;
  padding: 12px;
  border: 2px solid #e2e8f0;
  border-radius: 8px;
  font-size: 1em;
}

.todo-input input:focus {
  outline: none;
  border-color: #667eea;
}

.todo-list {
  list-style: none;
}

.todo-list li {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 15px;
  margin-bottom: 10px;
  background: #f7fafc;
  border-radius: 8px;
  transition: all 0.3s ease;
}

.todo-list li:hover {
  background: #edf2f7;
}

.todo-list li.completed span {
  text-decoration: line-through;
  color: #a0aec0;
}

.todo-list input[type="checkbox"] {
  width: 20px;
  height: 20px;
  cursor: pointer;
}

.todo-list span {
  flex: 1;
  font-size: 1.1em;
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

.btn-remove {
  background: #f56565;
  color: white;
  border: none;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  font-size: 1.5em;
  cursor: pointer;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
}

.btn-remove:hover {
  background: #e53e3e;
  transform: rotate(90deg);
}

.empty-message {
  text-align: center;
  color: #a0aec0;
  font-style: italic;
  padding: 20px;
}
</style>
