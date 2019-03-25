<template>
  <div class="projects">
    <b-container fluid class="mt-3">
      <b-row align-h="end">
        <b-col cols="10">
          <!---------- FADE CARD 1 ----------------->
          <div class="box outline">
            <b-img
              :src="require('../assets/i-vue2.png')"
              fluid
              alt="Responsive image"
              class="pt-3"
            />
            <div class="top-border">
              <h3>I Do With Vue</h3>
              <b-button variant="secondary" class="p-1" @click="toggleShow">View</b-button>
            </div>

            <transition name="fade">
              <b-button class="p-0" v-if="isShowing" @click="toggleShow">
                <div class="shade py-2">
                  <h3>Wedding RSVP Website</h3>
                  <h5>Built with Vue, Firebase and Firestore</h5>
                  <b-button
                    variant="outline-light"
                    size="sm"
                    class="mr-1"
                    href="https://www.dineenlauren.com/i-do-with-vue/#/"
                  >Site</b-button>
                  <b-button
                    variant="outline-light"
                    size="sm"
                    class="ml-1"
                    href="https://github.com/dineensch/i-do-with-vue"
                  >Repo</b-button>
                  <p class="mt-5">Click to close.</p>
                </div>
              </b-button>
            </transition>
          </div>
        </b-col>
        <b-col cols="10">
          <!---------- FADE CARD ----------------->
          <div class="box outline">
            <b-img
              :src="require('../assets/i-vue2.png')"
              fluid
              alt="Responsive image"
              class="pt-3"
            />
            <div class="top-border">
              <h3>I Do With Vue</h3>
              <b-button variant="secondary" class="p-1" @click="toggleShow" v-if="!isShowing">View</b-button>
            </div>

            <transition name="fade">
              <b-button class="p-0" v-if="isShowing" v-on:click="toggleShow">
                <div class="shade py-2">
                  <h3>Wedding RSVP Website</h3>
                  <h5>Built with Vue, Firebase and Firestore</h5>
                  <b-button
                    variant="outline-light"
                    size="sm"
                    class="mr-1"
                    href="https://www.dineenlauren.com/i-do-with-vue/#/"
                  >Site</b-button>
                  <b-button
                    variant="outline-light"
                    size="sm"
                    class="ml-1"
                    href="https://github.com/dineensch/i-do-with-vue"
                  >Repo</b-button>
                  <p class="mt-5">Click to close.</p>
                </div>
              </b-button>
            </transition>
          </div>
        </b-col>
        <b-col cols="10">
          <!---------- FADE CARD ----------------->
          <!-- <div class="box outline">
            <b-img
              :src="require('../assets/i-vue2.png')"
              fluid
              alt="Responsive image"
              class="pt-3"
            />
            <div class="top-border">
              <h3>I Do With Vue</h3>
              <b-button
                variant="secondary"
                class="p-1"
                v-on:click="[showBox = !showBox], [hideBtn = !hideBtn]"
                v-if="hideBtn"
              >View</b-button>
            </div>

            <transition name="fade">
              <b-button
                class="p-0"
                v-if="showBox"
                v-on:click="[showBox = !showBox], [hideBtn = !hideBtn]"
              >
                <div v-if="showBox" class="shade py-2">
                  <h3>Wedding RSVP Website</h3>
                  <h5>Built with Vue, Firebase and Firestore</h5>
                  <b-button
                    variant="outline-light"
                    size="sm"
                    class="mr-1"
                    href="https://www.dineenlauren.com/i-do-with-vue/#/"
                  >Site</b-button>
                  <b-button
                    variant="outline-light"
                    size="sm"
                    class="ml-1"
                    href="https://github.com/dineensch/i-do-with-vue"
                  >Repo</b-button>
                  <p class="mt-5">Click to close.</p>
                </div>
              </b-button>
            </transition>
          </div>-->
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
      isShowing: false
    };
  },
  methods: {
    toggleShow() {
      this.isShowing = !this.isShowing;
    }
  }
};
</script>



<style scoped>
.box {
  position: relative;
}
.img {
  width: 100%;
}
.shade {
  width: 100%;
  height: 100%;
  background-color: #070707d7;
  color: white;
  position: absolute;
  top: 0;
  left: 0;
}

.outline {
  padding: 0.25rem;
  background-color: #fff;
  border: 3px solid #dee2e6;
  border-radius: 0.25rem;
  max-width: 100%;
  height: auto;
}
.top-border {
  border-top: 3px solid #dee2e6;
}
p {
  font-family: brandon-grotesque, sans-serif;
  font-weight: 100;
  font-style: normal;
}
</style>
