<template>
  <b-container fluid class="m-0 p-0">
    <b-jumbotron>
      <h5>Dineen Lauren</h5>
      <b-button size="sm" variant="dark" href="#">Learn More</b-button>
    </b-jumbotron>

    <!-- <div class="bg-circle-1 bg-circle"></div>
    <div class="bg-circle-2 bg-circle"></div>
    <div class="bg-circle-3 bg-circle"></div>
    <div class="bg-circle-4 bg-circle"></div>-->
  </b-container>
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
  font-size: 3rem;
  padding-left: 10px;
  font-weight: 300;
  line-height: 1;
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
