<template>
  <div class="about-grid office">
    <div class="top-left office">
      <Heading :pageTitle="pageTitle" />
    </div>
    <div class="top-right office">
      <Nav />
    </div>
    <div class="bottom-left office">
      <img class="galaxy" src="../assets/explode.svg" alt />
    </div>
    <div class="bottom-right office">
      <img class="out-img" src="../assets/hobbie.png" alt="Profile shot in Utah mountains" />
      <img class="explode" src="../assets/galaxy.svg" alt />

      <h2 class="about-header">Out of Office</h2>
      <p
        class="desc"
      >When I'm not in the office I like to experience the outdoors. Rock climbing is the way I try to spend most of my free time. It's the perfect combination of mental and physical, it requires maximum effort in both. Like in life, if you're not falling you're not trying hard enough.</p>
    </div>
  </div>
</template>

<script>
import Heading from './Heading'
export default {
  components: {
    Heading,
  },
  data() {
    return {
      pageTitle: 'Learn About Me',
    }
  },
}
</script>

<style lang="scss">
.about-grid {
  .out-img {
    width: 23vw;
    position: fixed;
    left: 19vw;
    top: 25vh;
  }
  &.office {
    .desc,
    .about-header,
    a {
      color: white;
    }
    .heading {
      .line {
        background-color: $primary;
      }
      h3 {
        color: $primary;
      }
    }
    .top-left,
    .bottom-left {
      background-color: white;
    }
    .bottom-right,
    .top-right {
      background-color: $primary;
    }
  }
}
</style>