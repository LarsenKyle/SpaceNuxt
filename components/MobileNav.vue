<template>
  <footer>
    <nav class="mobile">
      <div v-if="false" class="home">
        <v-icon @click="navTo" id="home-icon">mdi-home</v-icon>
        <p @click="navTo">Home</p>
      </div>
      <div class="work">
        <v-icon @click="navTo" class="mr-1" id="work-icon">mdi-xml</v-icon>
        <p @click="navTo">Work</p>
      </div>
      <div class="about">
        <v-icon @click="navTo" id="about-icon">mdi-account</v-icon>
        <p @click="navTo">About</p>
      </div>
      <div class="contact">
        <v-icon @click="navTo" class="ml-2" id="contact-icon">mdi-chat</v-icon>
        <p @click="navTo">Contact</p>
      </div>
    </nav>
  </footer>
</template>

<script>
export default {
  methods: {
    navTo(e) {
      let path = e.target.parentNode.className
      if (path === 'home') {
        path = '/'
      }
      this.$router.push({
        path: path,
      })
    },
  },
}
</script>

<style lang="scss">
.mobile {
  background-color: $primary;
  position: fixed;
  width: 100vw;
  display: flex;
  bottom: 0vh;
  justify-content: space-around;
  color: white;
  font-size: 1.3rem;
}
#contact-icon,
#about-icon,
#work-icon,
#home-icon {
  color: white;
  font-size: 3.5rem;
  padding-top: 1rem;
}
</style>