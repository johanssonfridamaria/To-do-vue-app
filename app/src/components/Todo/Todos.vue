<template>
  <div>
    <div class="todo mt-2 d-flex">
      texttexttext<button class="delete-btn">X</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Todos",
};
</script>

<style>
.todo {
  background-color: #fff;
  width: 100%;
  padding: 0.7rem 1rem;
  border: 0.1rem solid #ccc;
  border-radius: 0.5rem;
  font-size: 1rem;
  outline: none;
  justify-content: space-between;
  align-items: center;
}
.delete-btn {
  background-color: transparent;
  border-radius: 50%;
  padding:0;
  font-weight: bold;
  color: #ccc;
  font-size: 1.5rem;
}
</style>