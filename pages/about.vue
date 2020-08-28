<template>
  <v-layout>
    <MobileAbout />
    <div v-if="!office" class="about-grid">
      <div class="top-left">
        <Heading :pageTitle="pageTitle" />
      </div>
      <div class="top-right">
        <Nav />
      </div>
      <div class="bottom-left">
        <img class="galaxy" src="../assets/galaxy.svg" alt />
        <img class="about-img" src="../assets/about.png" alt="Profile shot in Utah mountains" />
      </div>
      <div class="bottom-right">
        <img class="explode" src="../assets/explode.svg" alt />

        <h2 class="about-header">Front-End Devloper</h2>
        <p
          class="desc long"
        >The most exciting thing about being a developer is there is aways something to learn and always room for improvment. As a developer I have a strong understanding of the JavaScript, HTML and CSS. This makes picking up new frameworks much easier and makes me much more flexible as a developer. Vue is my prefered development enviroment. Wether createing a SPA PWA, native app or even desktop apps Vue makes the proccess simple and streamlined..</p>
      </div>
    </div>
    <OutOfOffice v-if="office" />
    <Next v-if="!office" @clicked="showNext" />
    <Back v-if="office" @clicked="showNext" />
  </v-layout>
</template>

<script>
import MobileAbout from '../components/MobileAbout'

import Next from '../components/Next'
import OutOfOffice from '../components/OutOfOffice'
export default {
  data() {
    return {
      pageTitle: 'Learn About Me',
      office: false,
    }
  },
  components: {
    Next,
    OutOfOffice,

    MobileAbout,
  },
  methods: {
    showNext(value) {
      this.office = !this.office
    },
  },
}
</script>

<style lang="scss">
.explode {
  position: fixed;
  top: 9vh;
  right: 3vw;
  width: 10vw;
}
.galaxy {
  position: fixed;
  bottom: 8vh;
  left: 3vw;
  width: 10vw;
}
.about-grid {
  #right-mid {
    top: 50vh;
  }
  width: 100vw;
  display: grid;

  grid-template-columns: 30vw 70vw;
  grid-template-rows: 20% 80%;
  .heading {
    color: white;
    .line {
      background-color: white;
    }
  }
  .top-left,
  .bottom-left {
    background-color: #a64de9;
    color: white;
  }
  .top-left {
    .line,
    h3 {
      position: relative;
      left: 5vw;
      top: 1vh;
    }
  }

  .about-img {
    margin-left: 20vw;
    margin-top: 5vh;
    width: 23vw;
  }
  .about-header,
  .desc {
    width: 22vw;

    color: #a64de9;
    margin-left: 15vw;
  }
  .desc {
    height: 40vh;
    overflow-y: auto;
    font-size: 1.2rem;
  }
  .about-header {
    margin-top: 10vh;
    font-size: 2.2rem;
  }
}
.mo-about {
  display: none;
}
@media only screen and (max-width: 900px) {
  .about-grid {
    display: none;
  }
  .mo-about {
    width: 100vw;
    display: flex;
    flex-direction: column;
    .mainImg {
      width: 70vw;
      margin: 0 auto;
    }
    img {
      width: 70vw;
    }
  }
  #right-mid {
    display: none;
  }
}
</style>