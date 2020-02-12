<template>
  <div class="jumbotron-fluid todo-header text-center">
    <div class="container">
      <h1 class="display-4">{{headerText}}</h1>
      <p class="lead">{{subText}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["headerText", "subText"]
};
</script>

<style scoped>
.todo-header {
  background-color: #1a1a1a;
  height: 150px;
  color: white;
  margin-bottom: 20px;
  padding: 10px;
}
</style>
