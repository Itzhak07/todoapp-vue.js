<template>
  <div class="todo-item" v-bind:class="{'is-complete': todo.completed}">
    <p>
      <input type="checkbox" v-on:change="markComplete" v-if="todo.completed" checked />
      <input type="checkbox" v-on:change="markComplete" v-else />
      {{todo.title}}
      <button @click="$emit('del-todo', todo.id)" class="del">
        <i class="fas fa-trash"></i>
      </button>
    </p>
  </div>
</template>

<script>

export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    }
  }
};
</script>

<style scoped>
.todo-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
}
.is-complete {
  text-decoration: line-through;
  background-color: rgb(204, 204, 204);
}
.del {
  background: #ff0000;
  color: #fff;
  border: none;
  padding: 5px 9px;
  border-radius: 50%;
  cursor: pointer;
  float: right;
}

.todo-item p {
  text-align: left;
  padding-left: 20px;
}
</style>