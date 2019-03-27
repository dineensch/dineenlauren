<template>
	<div>
		<b-jumbotron class="m-0 py-5">
			<h5>
				Dineen
				<span id="dineen">Lauren</span>
			</h5>
		</b-jumbotron>
		<div>
			<b-nav tabs class="d-flex justify-content-end mb-2">
				<b-nav-item
					class="filter"
					@click="activate(1)"
					:class="{ active : currentFilter === 1 }"
					href="#/"
				>About</b-nav-item>
				<b-nav-item
					class="filter"
					@click="activate(2)"
					:class="{ active : currentFilter === 2 }"
					href="#/projects"
				>Projects</b-nav-item>
				<b-nav-item
					class="filter"
					@click="activate(3)"
					:class="{ active : currentFilter === 3 }"
					href="#/about"
				>Contact</b-nav-item>
			</b-nav>
		</div>
	</div>
</template>

<script>
export default {
	name: "Hero",
	data() {
		return {
			currentFilter: 1
		};
	},
	methods: {
		activate: function(filter) {
			this.currentFilter = filter;
		}
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h5 {
	text-align: right;
	padding-left: 10px;
	line-height: 0.3;
	font-size: 2.4rem;
	font-family: ocr-a-std, monospace;
	font-weight: 400;
	font-style: normal;
}

span#dineen {
	font-family: american-scribe, sans-serif;
	font-weight: 400;
	font-style: normal;
	font-size: 4.5rem;
}

ul {
	list-style-type: none;
	padding: 0;
}
li {
	display: inline-block;
	margin: 0 10px;
}
a {
	color: rgb(48, 48, 48);
}
.nav-link {
	text-align: right;
	padding: 0;
}
</style>
