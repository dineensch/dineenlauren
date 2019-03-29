<template>
	<div class="projects">
		<b-container fluid class="mt-3">
			<b-row align-h="end">
				<b-col cols="10" md="3" v-for="(box, index) in boxes" :key="box.id" @click="toggleShow(index)">
					<div class="box">
						<div class="img-contain">
							<b-img v-bind:src="box.image" fluid-grow alt="Responsive image"/>
							<div class="overlay py-5">
								<b-button class="overlay-text mt-4 py-0">View</b-button>
							</div>

							<transition name="fade">
								<div class="shade" v-if="box.isShowing">
									<div class="shade-content">
										<h3>What it is:</h3>
										<p>{{ box.info }}</p>
										<h3>Built With:</h3>
										<p>{{ box.built }}</p>
										<b-button v-bind="btnStyle" v-bind:href="box.siteLink" class="mr-1">View</b-button>
										<b-button v-bind="btnStyle" v-bind:href="box.repoLink" class="ml-1">Code</b-button>
										<b-button variant="light" size="sm" class="d-block mx-auto my-2 px-1 py-0">Close</b-button>
									</div>
								</div>
							</transition>
						</div>

						<div class="card-content py-2 mb-4">
							<h3>{{ box.title }}</h3>
						</div>
					</div>
				</b-col>
			</b-row>
		</b-container>
	</div>
</template>



<script>
export default {
	name: "Projects",
	data() {
		return {
			btnStyle: { class: "btn-sm btn-outline-light px-1 py-0" },
			boxes: [
				{
					isShowing: false,
					title: "Wedding RSVP",
					info:
						"A wedding website template that provides important information and RSVP capabilities",
					built: "Vue, Firebase and Firestore",
					image: require("../assets/1.png"),
					siteLink: "https://www.dineenlauren.com/i-do-with-vue/#/",
					repoLink: "https://github.com/dineensch/i-do-with-vue"
				},
				{
					isShowing: false,
					title: "Potter Time",
					info:
						"App that calls APIs to generate fun reference material for Star Wars and Harry Potter.",
					image: require("../assets/2.png"),
					siteLink: "https://www.dineenlauren.com/i-do-with-vue/#/",
					repoLink: "https://github.com/dineensch/i-do-with-vue"
				},
				{
					isShowing: false,
					title: "Weather App",
					info:
						"App that caches using localStorage. Search for current weather statistics of your favorite cities.",
					image: require("../assets/3.png"),
					siteLink: "https://www.dineenlauren.com/i-do-with-vue/#/",
					repoLink: "https://github.com/dineensch/i-do-with-vue"
				},
				{
					isShowing: false,
					title: "Tic Tac Toe",
					info: "Interactive browser game you can play with a friend!",
					image: require("../assets/4.png"),
					siteLink: "https://www.dineenlauren.com/i-do-with-vue/#/",
					repoLink: "https://github.com/dineensch/i-do-with-vue"
				},
				{
					isShowing: false,
					title: "Image Maker",
					info: "Create your own meme!",
					image: require("../assets/5.png"),
					siteLink: "https://www.dineenlauren.com/i-do-with-vue/#/",
					repoLink: "https://github.com/dineensch/i-do-with-vue"
				},
				{
					isShowing: false,
					title: "API Superstore",
					info: "One-page scroll website with a professional business layout",
					image: require("../assets/6.png"),
					siteLink: "https://www.dineenlauren.com/i-do-with-vue/#/",
					repoLink: "https://github.com/dineensch/i-do-with-vue"
				}
			]
		};
	},
	methods: {
		toggleShow(i) {
			this.boxes[i].isShowing = !this.boxes[i].isShowing;
		}
	}
};
</script>



<style scoped>
.box {
	position: relative;
}

img {
	padding: 0.25rem;
	background-color: #fff;
	border: 1px solid black;
	border-radius: 0.25rem;
}

.shade {
	width: 100%;
	height: 100%;
	background-color: #070707d7;
	border: 1px solid #fff;
	padding: 0.25rem;
	border-radius: 0.25rem;
	color: white;
	position: absolute;
	top: 0;
	left: 0;
}

.shade-content {
	width: 100%;
	height: 100%;
	border: 1px solid #fff;
	border-radius: 0.25rem;
	color: white;
}

.card-content {
	background-color: black;
	border-radius: 0 0 0.25rem 0.25rem;
}
p {
	font-family: brandon-grotesque, sans-serif;
	font-size: 1rem;
	font-weight: 100;
	line-height: 1.3;
	margin-bottom: 0.25rems !important;
}

h3 {
	font-size: 1.5rem;
	color: white;
}

.overlay {
	width: 100%;
	height: 100%;
	opacity: 1;
	background: #0707077a;
	border-radius: 0.25rem;
	overflow: hidden;
	position: absolute;
	top: 0;
	left: 0;
	cursor: pointer;
}

.overlay-text {
	font-size: 1.2rem;
	font-weight: 400;
	width: 100%;
	color: white;
	border: 1px solid white;
	background: #633637bb;
}

.img-contain {
	position: relative;
}

.fade-enter-active,
.fade-leave-active {
	transition: opacity 0.5s ease-out;
}

.fade-enter,
.fade-leave-to {
	opacity: 0;
}

/* Extra small devices (portrait phones, less than 576px) */
@media (min-width: 425.98px) {
	.overlay {
		opacity: 0;
	}

	.overlay:hover {
		opacity: 1;
		border-radius: 0.25rem;
		background: #07070773;
		transition: 0.3s opacity ease-out;
		cursor: pointer;
	}

	.overlay-text {
		padding-top: 10rem;
		font-size: 2rem;
		font-weight: 300;
	}
}

/* Small devices (landscape phones, less than 768px) */
@media (min-width: 576px) and (max-width: 767.98px) {
}

/* Medium devices (tablets, less than 992px) */
@media (min-width: 768px) and (max-width: 991.98px) {
}

/* Large devices (desktops, less than 1200px) */
@media (min-width: 992px) and (max-width: 1199.98px) {
}

/* Extra large devices (large desktops, 1200px and up) */
@media (min-width: 1200px) {
}
</style>


