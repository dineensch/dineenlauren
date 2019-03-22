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
	font-family: brandon-grotesque, sans-serif;
	font-weight: 100;
	font-style: normal;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
}
</style>
