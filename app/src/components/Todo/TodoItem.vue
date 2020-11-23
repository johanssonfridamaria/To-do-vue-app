<template>
  <li class="d-flex"> {{ todo.title }} <button class="delete-btn">X</button></li>
</template>

<script>

export default {
name: 'TodoItem',
props:['todo']
}
</script>

<style scooped>
.delete-btn {
  background-color: red;
  font-weight: bold;
  color: #fff;
  font-size: 1.5rem;
}
li{
  margin-bottom: 1rem;
  justify-content: space-between;
  align-items: center;
}
</style>