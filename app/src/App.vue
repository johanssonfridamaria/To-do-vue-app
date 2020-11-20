<template>
  <div>
    <appheader> 
    </appheader>
    <div class="container"></div>
  </div>
</template>

<script>
import Header from './components/Header';

export default {
  name: 'App',
  components: {
    appheader: Header,
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.container{
  width: 80%;
  margin: auto;
}
.d-flex{
  display: flex;
}
.mt-3
{
margin-top: 3rem;
}
</style>
