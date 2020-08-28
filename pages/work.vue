<template>
  <v-layout>
    <WorkShowcase :key="activeSlide.title" :work="activeSlide" />

    <MobileWork @clicked="showNext" :work="activeSlide" />

    <Next @clicked="showNext" />
  </v-layout>
</template>
<script>
import WorkShowcase from '../components/WorkShowcase'
import MobileWork from '../components/MobileWork'
import Next from '../components/Next'
export default {
  data() {
    return {
      workSlide: [
        {
          title: 'Project Set',
          source: '/ nuxt/assets/projectset.png',
          code: 'https://github.com/LarsenKyle/Project-Set',
          code: 'https://github.com/LarsenKyle/Project-Set',
          link: '',
          description:
            'Built with Vue and Firebase Project Set is a simple solution for managing route setting programs in a climbing gym ',
        },

        {
          title: 'Ten Sleep Yoga',
          source: '../assets/yoga.png',
          link: 'https://geoapp-a5e8c.firebaseapp.com/',
          code: 'https://github.com/LarsenKyle/WorlandYoga',
          description:
            'This web application is built with Vue. Built for a yoga studio in Tensleep this application keeps track of class attendance and clients. This application generates monthley and tracks yoga passes. Check out the demo version and play around if you like, click the link above ',
        },
        {
          title: 'Schooley and Sons Tackle',
          source: '../assets/schooley.png',
          link: 'https://schooleyicetackle.com/',
          code: 'https://github.com/LarsenKyle/schooleyicetackle',
          description:
            'An E-commerce website designed for a small tackle company in northern Michigan. This is update to an old site now makes is responsive and much simpler to navigate and purchase. ',
        },
      ],
      activeSlide: {
        title: 'Project Set',
        source: '../assets/projectset.png',
        code: 'https://github.com/LarsenKyle/Project-Set',
        link: '',
        description:
          'Built with Vue and Firebase Project Set is a simple solution for managing route setting programs in a climbing gym ',
      },
    }
  },
  components: {
    WorkShowcase,
    Next,
  },
  methods: {
    showNext(value) {
      let slideLength = this.workSlide.length
      let slideIndex = this.workSlide.findIndex(
        (slide) => slide.title === this.activeSlide.title
      )
      slideIndex += value

      if (slideLength === slideIndex) {
        slideIndex = 0
      }
      if (slideIndex === -1) {
        slideIndex = 2
      }
      this.activeSlide = this.workSlide[slideIndex]
    },
  },
}
</script>
<style lang="scss">
.mobile-work {
  display: none;
}
.btn {
  a {
    color: white;
    width: 100%;

    text-decoration: none;
  }
}
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
@media only screen and (min-width: 1450px) {
  .grid-container {
    .footer {
      .img-move {
        bottom: 26vh;
      }
    }
  }
}
@media only screen and (max-width: 1000px) {
  .grid-container {
    display: none;
  }
  .mobile-work {
    display: initial;
  }
  #right-mid {
    display: none;
  }
}
</style>