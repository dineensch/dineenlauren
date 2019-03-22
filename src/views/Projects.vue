<template>
	<div class="projects">
		<b-container fluid class="mt-3">
			<!-- <b-row align-h="end">
				<b-col cols="10">
					<div id="cardFade">
						<div class="card" id="card1">
							<div class="card-content">
								<div class="outline circle rounded-circle">
									<img
										src="../assets/idovue.png"
										class="d-inline-block align-middle"
										width="200"
										height="200"
										fluid
										alt="Responsive image"
									>
								</div>
								<h3>I Do With Vue</h3>
								<b-button v-on:click="show = !show">View More</b-button>
							</div>
						</div>
					</div>
				</b-col>
			</b-row>-->
			<b-row align-h="end">
				<b-col cols="10">
					<div id="fadeCard">
						<div class="outline circle rounded-circle">
							<img
								src="../assets/idovue.png"
								class="d-inline-block align-middle"
								width="200"
								height="200"
								fluid
								alt="Responsive image"
							>
							<h3>I Do With Vue</h3>
							<button v-on:click="show = true">View More</button>
						</div>
						<transition name="fade">
							<div v-if="show" class="card-drk">
								<h3>Wedding RSVP Website</h3>
								<h5>Built with Vue, Firebase, Firestore</h5>
								<button v-on:click="show = !show">View More</button>
							</div>
						</transition>
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
			show: false
		};
	}
};
</script>



<style scoped>
.outline {
	border: 2px solid #272727;
}
div.circle {
	height: 200px;
	width: 200px;
}

.card-drk {
	background-color: #633637ab;
	color: white;
	border: 1spx solid #633637;
}

p {
	font-family: brandon-grotesque, sans-serif;
	font-weight: 100;
	font-style: normal;
}

.btn-secondary {
	background-color: transparent;
	color: #272727;
	border: none;
}
.card {
	border: none !important;
}

.fade-enter-active,
.fade-leave-active {
	transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
	opacity: 0;
}
</style>
