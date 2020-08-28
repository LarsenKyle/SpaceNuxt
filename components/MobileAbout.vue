<template>
  <div class="mo-about">
    <div class="mainImg mt-5">
      <img src="../assets/about.png" alt />
    </div>
    <div class="words">
      <h3>Front-End Developer</h3>
      <p>The most exciting thing about being a developer is there is aways something to learn and always room for improvment. As a developer I have a strong understanding of the JavaScript, HTML and CSS. This makes picking up new frameworks much easier and makes me much more flexible as a developer. Vue is my prefered development enviroment. Wether createing a SPA PWA, native app or even desktop apps Vue makes the proccess simple and streamlined.</p>
    </div>
    <MobileNav />
  </div>
</template>

<script>
import MobileNav from '../components/MobileNav'
export default {
  components: {
    MobileNav,
  },
}
</script>

<style lang="scss">
.words {
  text-align: center;
  color: $primary;
  p {
    width: 90vw;
    margin: 0 auto;
    font-size: 1.2rem;
    margin-bottom: 150px;
  }
}
</style>