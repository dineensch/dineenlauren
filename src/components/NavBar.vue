<template>
	<b-container fluid class="m-0 p-0">
		<b-navbar toggleable="lg" type="dark" sticky>
			<b-navbar-brand href="#/" class="nav-logo m-0 p-0" height="30">
				<img
					src="../assets/dl_icon.png"
					height="40"
					width="40"
					class="d-inline-block align-middle"
					alt="Dineen Lauren icon"
				>
			</b-navbar-brand>

			<b-navbar-toggle target="nav_collapse"/>

			<b-collapse is-nav id="nav_collapse" class="p-0">
				<!-- Right aligned nav items -->
				<b-navbar-nav class="ml-auto">
					<b-navbar-nav class="nav-text">
						<b-nav-item href="#/about">About</b-nav-item>
						<b-nav-item href="#/projects">Projects</b-nav-item>
						<b-nav-item href="#/contact">Contact</b-nav-item>
					</b-navbar-nav>
				</b-navbar-nav>
			</b-collapse>
		</b-navbar>
	</b-container>
</template>

<script>
export default {
	name: "NavBar",
	props: {
		msg: String
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sticky-top {
	z-index: 100 !important;
}
.pgtitle {
	color: white;
	text-decoration: none;
}

nav.navbar {
	background-color: #363436;
	padding: 0.5rem 1rem;
}
.navbar-toggler {
	font-size: 1rem !important;
	border-color: rgba(255, 255, 255, 0.5) !important;
}

a {
	color: white;
}

a.nav-link {
	font-family: brandon-grotesque, sans-serif;
	font-weight: 300;
	font-style: normal;
	text-decoration: none;
	font-size: 1.9rem;
	font-weight: 200;
	line-height: 1.2;
	color: rgba(255, 255, 255, 0.7) !important;
}
a.nav-link:hover {
	color: rgba(255, 255, 255) !important;
}

/* Small devices (landscape phones, 576px and up) */
@media (min-width: 576px) and (max-width: 767.98px) {
	.nav-text {
		font-size: 25px;
	}
	div.nav-logo {
		visibility: hidden !important;
	}
}

/* Medium devices (tablets, 768px and up) */
@media (min-width: 768px) and (max-width: 991.98px) {
	a.nav-link {
		font-size: 1.4rem;
	}
}

/* Large devices (desktops, 992px and up) */
@media (min-width: 992px) and (max-width: 1199.98px) {
}

/* Extra large devices (large desktops, 1200px and up) */
@media (min-width: 1200px) {
	a.navbar-brand {
		font-size: 2.5rem;
	}
	a.nav-link {
		font-size: 1.5rem;
	}

	nav.navbar {
		line-height: 1;
	}
}
</style>

