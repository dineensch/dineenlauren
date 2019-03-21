<template>
  <div id="app">
    <vert-nav id="vertNav"></vert-nav>
    <nav-bar></nav-bar>
    <Hero></Hero>
    <router-view/>
  </div>
</template>

<script>
// @ is an alias to /src
import VertNav from "@/components/VertNav.vue";
import Hero from "@/components/Hero.vue";
import NavBar from "@/components/NavBar.vue";

export default {
  name: "home",
  components: {
    Hero,
    NavBar,
    VertNav
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
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
