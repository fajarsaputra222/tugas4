<template>
    <div>
      <select v-model="selectedCategory">
        <option value="All">All</option>
        <option value="Work">Work</option>
        <option value="Personal">Personal</option>
        <!-- Tambahkan opsi kategori lain jika diperlukan -->
      </select>
  
      <ul>
        <li v-for="task in filteredTasks" :key="task.id">
          {{ task.title }} - {{ task.category }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        tasks: [
          { id: 1, title: 'Task 1', category: 'Work' },
          { id: 2, title: 'Task 2', category: 'Personal' },
          // ...
        ],
        selectedCategory: 'All'
      };
    },
    computed: {
      filteredTasks() {
        const selectedCategory = this.selectedCategory;
  
        if (selectedCategory === 'All') {
          return this.tasks;
        }
  
        return this.tasks.filter(task => task.category === selectedCategory);
      }
    },
    watch: {
      selectedCategory: function(newCategory, oldCategory) {
        // Di sini Anda dapat memanggil fungsi atau metode lain jika diperlukan
      }
    }
  };
  </script>
  