<template>
  <v-layout class="grid-container">
    <div class="top-left">
      <Heading :pageTitle="pageTitle" />
    </div>
    <div class="top-right">
      <Nav />
      <div class="work-area">
        <p class="work-name">Project Set</p>
        <v-btn depressed height="55px" color="#a64de9" class="btn">Visit Site</v-btn>
        <v-btn depressed height="55px" color="#a64de9" class="btn">View Code</v-btn>
      </div>
    </div>

    <div class="footer">
      <img class="img-move" src="../assets/projectset.png" alt />
    </div>
    <div class="desc">
      <p>
        Built with Vue and Firebase Project Set is a
        simple solution for managing route setting
        programs in a climbing gym
      </p>
    </div>
  </v-layout>
</template>
<script>
import Nav from '../components/Nav'
import Heading from '../components/Heading'
export default {
  data() {
    return {
      pageTitle: 'Work',
    }
  },
  components: {
    Nav,
    Heading,
  },
}
</script>
<style lang="scss">
.grid-container {
  .top-left {
    grid-area: heading;
    position: relative;
    left: 5vw;
  }
  .top-right {
    display: grid;
    grid-template-rows: 70% auto;
    grid-area: main-nav;
    .work-area {
      color: #a64de9;
      font-size: 1.5rem;
      margin-left: 2vw;
      .work-name {
        font-size: 3rem;
      }
      .btn {
        color: white;
        width: 10vw;
      }
    }
  }

  .footer {
    .img-move {
      width: 45vw;
      position: relative;
      left: 5vw;
      bottom: 16vh;
      border-radius: 7px;
    }
    background-color: #a64de9;
    grid-area: footer;
  }
  .desc {
    grid-area: desc;
    background-color: #a64de9;
    color: white;
    font-size: 1.5rem;
    p {
      margin-top: 3rem;
      margin-left: 2vw;
      margin-right: 20vw;
    }
  }
  display: grid;

  grid-template-columns: 50% 50%;
  grid-template-rows: auto 40%;
  grid-template-areas:
    'heading main-nav'
    'footer desc';
}
</style>