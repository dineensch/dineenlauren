<template>
	<div class="about container">
		<div class="box" v-for="(box, index) in boxes" :key="box" @click="toggleShow(index)">
			<button v-if="!box.isShowing">View {{ index + 1 }}</button>
			<div class="shade" v-if="box.isShowing">
				<button>Close {{ index + 1 }}</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "About",
	data() {
		return {
			boxes: [{ isShowing: false }, { isShowing: false }, { isShowing: false }]
		};
	},
	methods: {
		toggleShow(i) {
			this.boxes[i].isShowing = !this.boxes[i].isShowing;
		}
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
	display: flex;
	flex-wrap: wrap;
}

.box {
	position: relative;
	height: 100px;
	width: 200px;
	margin: 10px;
	line-height: 75px;
	border: solid 1px black;
}

.shade {
	position: absolute;
	height: 100%;
	width: 100%;
	top: 0;
	left: 0;
	background-color: #07070771;
}
</style>
