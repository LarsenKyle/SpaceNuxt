<template>
  <v-layout class="bg-img">
    <WorkBtn class="action" />
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
  background-position: right;
  background-repeat: no-repeat;
  background-size: contain;
  .action{
    margin-right: 15rem;
  }
}
@media only screen and (max-width: 1500px) {
  .bg-img {
    background-position: bottom;
    background-size: cover;
  }
}


</style>