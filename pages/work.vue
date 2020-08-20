<template>
  <v-layout >
    <WorkShowcase :key="activeSlide.title" :work="activeSlide" />
    <Next @clicked="showNext" />
  </v-layout>
</template>
<script>
import WorkShowcase from '../components/WorkShowcase'
import Next from '../components/Next'
export default {
  data() {
    return {
      workSlide:[
        {
          title: "Project Set",
          source: "../assets/projectset.png",
          description: "Built with Vue and Firebase Project Set is a simple solution for managing route setting programs in a climbing gym "
        },
    
        {
          title: "Ten Sleep Yoga",
          source: "../assets/projectset.png",
          description: "Built with Vue and Firebase Project Set is a simple solution for managing route setting programs in a climbing gym "
        },
        {
          title: "Schooley and Sons Tackle",
          source: "../assets/projectset.png",
          description: "Built with Vue and Firebase Project Set is a simple solution for managing route setting programs in a climbing gym "
        }
      ],
      activeSlide:{
          title: "Project Set",
          source: "../assets/projectset.png",
          description: "Built with Vue and Firebase Project Set is a simple solution for managing route setting programs in a climbing gym "
        }
    }
  },
  components: {
    WorkShowcase,
    Next
  },
  methods:{
    showNext(value){
      let slideLength = this.workSlide.length
      let slideIndex = this.workSlide.findIndex(slide => slide.title === this.activeSlide.title)
      slideIndex += 1
      
      if(slideLength === slideIndex){
        slideIndex = 0
      }
     
     this.activeSlide = this.workSlide[slideIndex]
     
    
    }
  }
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
@media only screen and (min-width: 1450px) {
  .grid-container{
 .footer{
   .img-move{
     bottom: 26vh;
   }
 }}
}
</style>