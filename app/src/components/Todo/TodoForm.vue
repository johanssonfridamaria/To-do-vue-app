<template>
  <form class="d-flex" @submit.prevent="onSubmit">
    <div class="input-group d-flex">
      <input
        v-model="title"
        type="text"
        placeholder="Add todo..."
        :class="error ? {invalid:true} : {valid: true}"
      />
      <button type="submit" value="Submit">Add</button>
    </div>
    <span>{{ error }}</span>
  </form>
</template>

<script>
export default {
  name: "TodoForm",
  data() {
    return {
      id: null,
      title: "",
      completed: false,
      error: "",
    };
  },
  methods: {
    onSubmit() {
      if (this.title) {
        let todo = {
          id: Date.now(),
          title: this.title,
          completed: this.completed,
        };
        this.$emit("form-submitted", todo);
        this.id = null,
         this.title = null;
      } else {
        if (!this.title || this.title.length <2)
          this.error="Please insert atleast 2 characters";
      }
    },
  },
};
</script>

<style scooped>
form {
  flex-direction: column;
  width: 100%;
}
.input-group {
  flex-direction: row;
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

.invalid {
  border: 1px solid red;
  outline: red;
}
.valid {
  border: 1px solid green;
  outline: green;
}
</style>