<template>
  <v-layout class="bg-img">
    <WorkBtn />
    <Nav />
  </v-layout>
</template>

<script>
import Nav from '../components/Nav'
import WorkBtn from '../components/WorkBtn'
export default {
  components: {
    Nav,
    WorkBtn,
  },
}
</script>
<style lang="scss">
.bg-img {
  background-image: url('../assets/space.svg');

  /* Center and scale the image nicely */
  background-position: right;
  background-repeat: no-repeat;
  background-size: contain;
}
@media only screen and (max-width: 1500px) {
  .bg-img {
    background-position: bottom;
    background-size: cover;
  }
}
</style>