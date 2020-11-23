<template>
  <form class="d-flex">
    <input type="text" placeholder="Add todo..." />
    <button class="" type="submit">Add</button>
  </form>
</template>

<script>
export default {
  name: "TodoForm",
};
</script>

<style>
form {
  flex-direction: row;
  align-items: center;
}
input {
  width: 100%;
  padding: 0.7rem 1rem;
  margin: 0.5rem 0;
  display: inline-block;
  border: 0.1rem solid #ccc;
  border-radius: 0.5rem;
  font-size: 1rem;
  outline: none;
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