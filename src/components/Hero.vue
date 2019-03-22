<template>
	<b-jumbotron class="m-0 py-5">
		<h5>
			Dineen
			<span id="dineen">Lauren</span>
		</h5>
	</b-jumbotron>

	<!-- <div class="bg-circle-1 bg-circle"></div>
    <div class="bg-circle-2 bg-circle"></div>
    <div class="bg-circle-3 bg-circle"></div>
	<div class="bg-circle-4 bg-circle"></div>-->
</template>

<script>
export default {
	name: "Hero",
	props: {
		msg: String
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
	color: white;
}
</style>
