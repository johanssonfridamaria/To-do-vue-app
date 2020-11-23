<template>
  <div>
    <todoForm @form-submitted="addTodo"></todoForm>
    <div class="todo mt-2 d-flex">
      <h1>Todos</h1>
      <ul>
        <todo-item v-for="todo in todoList" :todo='todo' :key="todo.id"></todo-item>
      </ul>
    </div>
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue';
import TodoForm from './TodoForm';

export default {
  name: "TodoList",
  components: {
    TodoItem,
    TodoForm, 
  },
  data() {
    return {
      todoList: [],
    };
  },
  methods: {
    addTodo(todo) {
      this.todoList.push(todo);
    },
  },
};
</script>

<style scooped>
.todo {
  background-color: #fff;
  width: 100%;
  padding: 0.7rem 1rem;
  border: 0.1rem solid #ccc;
  border-radius: 0.5rem;
  flex-direction: column;
}
ul{
  list-style-type: none;
  margin: 2rem 0;
  padding: 0;
}


</style>