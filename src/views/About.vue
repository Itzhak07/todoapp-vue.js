<template>
  <div class="about">
    <Header headerText="About" />

    <div class="text-wrapper">
      <p>
        As a developer with passion for new technologies and a fan of both Recat & Angular, I wanted to put my hands on
        <span>Vue.js</span>.
      </p>
      <p>For a starting point, I've decided to write this Todo List App!</p>
      <p>
        I used
        Bootstrap for the UI the
        JSONPlaceholder API to GET, POST and DELETE todos.
      </p>
      <h3>Enjoy!</h3>
    </div>
  </div>
</template>

<script>
import Header from "../components/layout/Header.vue";

export default {
  name: "About",
  components: { Header }
};
</script>

<style scoped>
.text-wrapper {
  padding: 50px;
  max-width: 800px;
  margin: auto;
  text-align: left;
}
p {
  font-size: 22px;
}

span {
  color: #4fc08d;
}
</style>
