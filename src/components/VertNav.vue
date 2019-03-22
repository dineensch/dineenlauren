<template>
	<div>
		<b-nav vertical class="text-center vertList">
			<b-nav-item active>
				<font-awesome-icon :icon="['fab', 'github']"/>
			</b-nav-item>
			<b-nav-item>
				<font-awesome-icon :icon="['fab', 'linkedin']"/>
			</b-nav-item>
			<b-nav-item>
				<font-awesome-icon icon="envelope"/>
			</b-nav-item>
		</b-nav>
	</div>
</template>

<script>
export default {
	name: "VertNav"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div#vertNav {
	background-color: #212021a9;
	top: 0;
	left: 10px;
	height: 100%;
	width: 15%;
	position: fixed;
	z-index: 1020;
	overflow-x: hidden;
	padding-top: 10rem;
}

.vertList {
	margin-top: 3rem;
}
.nav-link {
	padding-left: 0.2rem;
	padding-right: 0.2rem;
	font-size: 1.8rem;
	color: #ffffff;
}

/* Extra small devices (portrait phones, less than 576px) */
@media (max-width: 575.98px) {
	div#vertNav {
		z-index: 100;
	}
}

/* Small devices (landscape phones, 576px and up) */
@media (min-width: 576px) and (max-width: 767.98px) {
}

/* Medium devices (tablets, 768px and up) */
@media (min-width: 768px) and (max-width: 991.98px) {
}

/* Large devices (desktops, 992px and up) */
@media (min-width: 992px) and (max-width: 1199.98px) {
}

/* Extra large devices (large desktops, 1200px and up) */
@media (min-width: 1200px) {
}
</style>

