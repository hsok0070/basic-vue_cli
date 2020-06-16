<template>
  <div id="app" class="container">
    <h1 class='text-center'>Todo app</h1>
    <input
    v-model='todoText' 
    type="text" 
    class='w-100 p-2' 
    placeholder="Type todo"
    @keyup.enter="addTodo"
    >
    <hr>
    <Todo 
    v-for="todo in todos" 
    :key="todo.id"
    :todo="todo"
    @toggle-checkbox='toggleCheckbox'
    @click-delete='deleteTodo'></Todo>
  </div>
</template>

<script>
import Todo from '@/components/Todo.vue';

export default {
  data() {
    return {
      todoText:'',
      todos: [
        { id: 1, text: 'buy a car', checked: false}, 
        { id: 2, text: 'play game', checked: false}, 
      ]
    }
  },
  components: {
    Todo
  },
  methods: {
    addTodo(e) {
      this.todos.push({
        id: Math.random(),
        text: e.target.value,
        checked: false,
        });
        this.todoText = '';
    },
    toggleCheckbox({id, checked}) {
      /* console.log(id,checked) */
      const index = this.todos.findIndex(todo => {
        return todo.id === id;
      });
      this.todos[index].checked = checked;
    },
    deleteTodo(id) {
      const index = this.todos.findIndex(todo => {
        return todo.id === id;
      });
      this.todos.splice(index, 1);
    }
  }
}
</script>
