<template>
  <div class="container add-todo-wrapper">
    <form @submit="addTodo">
      <input name="title" type="text" placeholder="Add Todo..." v-model="title" />

      <input class="btn" type="submit" value="Submit" />
    </form>
  </div>
</template>

<script>
import uuid from "uuid";

export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const newTodo = {
        id: uuid.v4(),
        title: this.title,
        completed: false
      };

      this.$emit("add-todo", newTodo);
      this.title = "";
    }
  }
};
</script>

<style  scoped>
form {
  display: flex;
  margin-bottom: 20px;
}
input[type="text"] {
  flex: 10;
  padding: 5px;
}
input[type="submit"] {
  flex: 2;
}
</style>