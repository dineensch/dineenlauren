<template>
	<div class="home">
		<b-container class="fluid">
			<b-row align-h="end">
				<b-col cols="10" order="1" class="p-1">
					<h2 class="mb-0">Who</h2>
					<hr class="my-1 mx-3">
					<p>
						My name is Dineen
						<br>and I am a full-stack designer with a background in sales and business operations.
					</p>
				</b-col>
				<b-col cols="10" class="p-1">
					<img
						src="../assets/bh2.png"
						class="d-inline-block align-middle"
						width="180"
						fluid
						alt="Responsive image"
					>
				</b-col>
			</b-row>
		</b-container>
		<b-container>
			<b-row align-h="end" class="mr-1">
				<b-col cols="9" md="12" class="p-1">
					<b-row align-h="center" class="ml-5">
						<b-col md="12" order="1" class="p-1">
							<h2 class="mb-0">What</h2>
							<hr class="my-1 mx-3">
							<p>
								I have a knack for
								<br>UX, UI and Front-End Development as well as an instinct for streamlining processes to promote efficiency.
							</p>
						</b-col>
						<b-col md="12" class="p-0" align-self="start">
							<div class="circle circle-drk rounded-circle">
								<p class="m-0 py-2">JS</p>
							</div>
						</b-col>
						<b-col class="p-0" align-self="center">
							<div class="circle circle-lt rounded-circle">
								<p class="m-0 py-2">vue</p>
							</div>
						</b-col>
						<b-col class="p-0" align-self="start">
							<div class="circle circle-drk rounded-circle">
								<p class="m-0 py-2">ux/ui</p>
							</div>
						</b-col>
						<b-col class="p-0" align-self="end">
							<div class="circle circle-lt rounded-circle">
								<p class="m-0 py-2">ps</p>
							</div>
						</b-col>
					</b-row>
				</b-col>
			</b-row>
		</b-container>
		<b-container class="fluid">
			<b-row align-h="end">
				<b-col cols="10" order="1" class="p-1">
					<h2 class="mb-0">About Me</h2>
					<hr class="my-1 mx-3">
					<p>Combining my work experience and technical based skillset allows me to understand office and team dynamic, as well as necessary web improvements. I aim for solutions that mix in personality with function while maintaining a client's needs.</p>
				</b-col>
				<b-col cols="10" class="p-1">
					<div class="outline p-1"></div>
				</b-col>
			</b-row>
		</b-container>
	</div>
</template>

<script>
export default {
	data() {
		return {
			boxes: [
				{
					isShowing: false
				}
			]
		};
	}
};
</script>

<style scoped>
.outline {
	border: 1px solid #633637;
}
.circle {
	height: 50px;
	width: 50px;
}

.circle-drk {
	background-color: #633637;
	color: white;
}
.circle-lt {
	border: 1px solid #633637;
	color: #633637;
}

.blue {
	border: solid 1px blue;
}

p {
	font-family: brandon-grotesque, sans-serif;
	font-weight: 100;
	font-style: normal;
}
</style>
