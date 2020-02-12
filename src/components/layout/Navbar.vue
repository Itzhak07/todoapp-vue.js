<template>
  <div id="nav">
    <router-link to="/">Home</router-link>|
    <router-link to="/about">About</router-link>
  </div>
</template>

<script>
export default {
  name: "Navbar"
};
</script>

<style scoped>
#nav {
  background-color: #1a1a1a;
}

#nav a {
  font-weight: bold;
  color: white;
  margin: 10px
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>