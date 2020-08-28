<template>
  <div class="mobile-work">
    <div class="color-block">
      <h3>Explore My Work</h3>
      <div class="slide-show">
        <v-icon @click="showNext" class="mr-4f" id="left">mdi-chevron-left</v-icon>
        <v-icon @click="showNext" class="ml-4" id="right">mdi-chevron-right</v-icon>
      </div>
      <img v-if="work.title === 'Project Set'" class="img-move" src="../assets/projectset.png" alt />
      <img v-if="work.title === 'Ten Sleep Yoga'" class="img-move" src="../assets/yoga.png" alt />
      <img
        v-if="work.title === 'Schooley and Sons Tackle'"
        class="img-move"
        src="../assets/schooley.png"
        alt
      />
    </div>
    <div class="project-info">
      <v-btn v-if="work.link.length > 1" depressed height="55px" color="#a64de9" class="btn">
        <a target="_blank" :href="work.link">Visit Site</a>
      </v-btn>
      <v-btn depressed height="55px" color="#a64de9" class="btn">
        <a target="_blank" :href="work.code">View Code</a>
      </v-btn>
      <h3>{{work.title}}</h3>
      <p>{{work.description}}</p>
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
  props: ['work'],
  data() {
    return {
      pageTitle: 'Explore My Work',
    }
  },
  methods: {
    showNext(e) {
      const val = e.target.id
      if (val === 'left') {
        this.$emit('clicked', -1)
      }
      if (val === 'right') {
        this.$emit('clicked', 1)
      }
    },
  },
}
</script>

<style lang="scss" >
.slide-show {
  text-align: center;
  position: relative;
  top: 2vh;
  #left,
  #right {
    color: white;
    font-size: 3rem;
  }
}

.mobile-work {
  width: 100%;
  .project-info {
    margin-bottom: 150px;
    .btn {
      color: white;
      margin-top: 15vh;
      margin-bottom: 3vh;
    }
    text-align: center;
    color: $primary;
    h3 {
      font-size: 2.3rem;
    }
    p {
      font-size: 1.7rem;
      width: 90vw;
      padding: 20px;
      border-radius: 5px;
      text-align: center;
      margin: 0 auto;
      background-color: #fffdf8;
    }
  }
}
.color-block {
  position: relative;
  width: 100%;
  background-color: $primary;
  height: 40vh;
  h3 {
    color: white;
    padding-top: 5vh;
    text-align: center;
  }
  .img-move {
    width: 90vw;
    position: absolute;
    margin-left: 5vw;
    bottom: -10vh;
  }
  .heading {
    h3 {
      color: white;
    }
    .line {
      background-color: white;
    }
  }
}
</style>