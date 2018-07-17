<template>
  <div id="app">
    <Navbar />
    <img src="./assets/helvetica icons x6-03-500x500.png" width="200">
    <Blog />
    <router-view/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
import About from "./components/About";
import Contact from "./components/Contact";
import SignIn from "./components/SignIn";
import SignUp from "./components/SignUp";
import Blog from "./components/Blog";

export default {
  name: "App",
  components: {
    Navbar,
    About,
    Contact,
    SignIn,
    SignUp,
    Blog
  },
  data() {
    return {

    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
li {
  display: inline-block;
  list-style-type: none;
  margin: 0;
}
</style>
