<template>
  <nav>
    <ul>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/contact">Contact</router-link>
      <router-link to="/blog">Blog</router-link>
      <router-link to="/sign-in">Sign In</router-link>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {};
  }
};
</script>

<style scoped>
nav {
  text-align: center;
}
nav ul {
  padding: 0;
}
nav ul li {
  display: inline-block;
  list-style-type: none;
  margin: 0;
}
nav a {
  text-decoration: none;
  padding: 5px;
  border-radius: 5px;
}
nav a:hover {
  background: rgba(50, 100, 250, 0.5);
}
</style>
