<template>
  <div class="grid-container">
    <div class="top-left">
      <Heading :pageTitle="pageTitle" />
    </div>
    <div class="top-right">
      <div>
        <Nav />
      </div>

      <div class="work-area">
        <p class="work-name">{{work.title}}</p>
        <v-btn v-if="work.link.length > 1" depressed height="55px" color="#a64de9" class="btn">
          <a target="_blank" :href="work.link">Visit Site</a>
        </v-btn>
        <v-btn depressed height="55px" color="#a64de9" class="btn">
          <a target="_blank" :href="work.code">View Code</a>
        </v-btn>
      </div>
    </div>

    <div class="footer">
      <img v-if="work.title === 'Project Set'" class="img-move" src="../assets/projectset.png" alt />
      <img v-if="work.title === 'Ten Sleep Yoga'" class="img-move" src="../assets/yoga.png" alt />
      <img
        v-if="work.title === 'Schooley and Sons Tackle'"
        class="img-move"
        src="../assets/schooley.png"
        alt
      />
    </div>
    <div class="desc">
      <p>{{work.description}}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pageTitle: 'Explore My Work',
    }
  },
  props: ['work'],
}
</script>

<style>
</style>