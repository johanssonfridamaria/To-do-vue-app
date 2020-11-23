<template>
  <li class="d-flex">
    {{ todo.title }}
    <delete-todobtn class="button" @click="removeTodo"></delete-todobtn>
  </li>
</template>

<script>
import DeleteTodobtn from "./DeleteTodobtn.vue";

export default {
  components: { DeleteTodobtn },
  name: "TodoItem",
  props: ["todo",],
  methods: {
    removeTodo(id) {
      for (var i = 0; i < this.todoList.length; i++) {
        if (this.todoList[i] === id) {
          this.todoList.splice(i, 1);
        }
      }
    },
  },
};
</script>

<style scooped>
.delete-btn {
  background-color: red;
  font-weight: bold;
  color: #fff;
  font-size: 1.5rem;
}
li {
  margin-bottom: 1rem;
  justify-content: space-between;
  align-items: center;
}
</style>