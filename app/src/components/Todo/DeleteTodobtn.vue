<template>
<button class="delete-btn" :click="onDelete">X</button>
</template>

<script>
export default {
name: 'DeleteTodoBtn',
props:['todo'],
  methods: {
    onDelete() {
      this.$emit('removeTodo',this.todo.id);
    },
  },
}
</script>

<style>

</style>