<template>
  <div>
    <appheader> 
    </appheader>
    <div class="mt-2 container">
      <todoForm>
      </todoForm>
      <todos>
      </todos>
    </div>
  </div>
</template>

<script>
import Header from './components/Header';
import TodoForm from './components/Todo/TodoForm'
import Todos from './components/Todo/Todos.vue';

export default {
  name: 'App',
  components: {
    appheader: Header,
    TodoForm,
    Todos,
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
</style>
