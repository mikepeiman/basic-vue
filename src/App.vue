<template>
  <div id="app">
    <Navbar />
    <img src="./assets/helvetica icons x6-03-500x500.png" width="200">
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
body {
  background: url("./assets/quote-bg-1.jpg") no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  margin-top: 60px;
  /* background-image: url("C:/Users/Mike/Desktop/udemy-vue-firebase/basic-vue/src/assets/catalyst-linkedin-bg-2.png"); */
}
li {
  display: inline-block;
  list-style-type: none;
  margin: 0;
}
</style>
