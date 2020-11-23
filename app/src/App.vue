<template>
  <div>
    <appheader> 
    </appheader>
    <div class="mt-2 container">
      <todoList></todoList>
    </div>
  </div>
</template>

<script>
import Header from './components/Header';
import TodoList from './components/Todo/TodoList.vue';

export default {
  name: 'App',
  components: {
    appheader: Header,
    TodoList,
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body{
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  background-color: #f443364d;
}
.container{
  width: 80%;
  margin: auto;
}
.d-flex{
  display: flex;
}
.mt-2
{
margin-top: 2rem;
}
button {
  padding: 0.7rem 1.5rem;
  background-color: #e91e634d;
  border: none;
  outline: none;
  border-radius: 0.5rem;
  font-size: 1rem;
  margin-left: 1.5rem;
  color: #fff;
  cursor: pointer;
}
</style>
