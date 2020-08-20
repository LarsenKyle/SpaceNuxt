<template>
  <v-layout  >
      <div v-if="!office" class="about-grid">
      <div class="top-left">
        <Heading :pageTitle="pageTitle" /> 
      </div>
      <div class="top-right">
         <Nav />
        
      </div>
      <div class="bottom-left">
          <img class="galaxy" src="../assets/galaxy.svg" alt="">
         <img class="about-img" src="../assets/about.png" alt="Profile shot in Utah mountains">
      </div>
      <div class="bottom-right">
           <img class="explode" src="../assets/explode.svg" alt="">
         
          <h2 class="about-header" >Front-End Devloper</h2>
          <p class="desc">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam beatae omnis praesentium fugiat odit illum dolor aliquam explicabo nesciunt, nisi deserunt adipisci! Quam libero quia voluptates enim! Expedita, voluptates accusantium.</p>
      </div>
      </div>
      <OutOfOffice v-if="office" />
       <Next v-if="!office" @clicked="showNext" />
       <Back v-if="office" @clicked="showNext" />
  </v-layout>
 
</template>

<script>
import Next from '../components/Next'
import OutOfOffice from '../components/OutOfOffice'
export default {
data(){
    return{
        pageTitle:"Learn About Me",
        office: false
    }
},
components: {
    Next,
    OutOfOffice
},
methods:{
    showNext(value){
      this.office = !this.office
   
    }
  }
}
</script>

<style lang="scss"> 
.explode{
    position: fixed;
    top: 9vh;
    right: 3vw;
    width: 10vw;
}
.galaxy{
    position: fixed;
    bottom: 8vh;
    left: 3vw;
    width: 10vw;
}
.about-grid{
    #right-mid{
        top: 50vh;
    }
    width: 100vw;
    display: grid;
    
    grid-template-columns: 30vw 70vw;
    grid-template-rows: 20% 80%;
     .heading{
        color: white;   
        .line{
             background-color: white;
             }
    }
     .top-left, .bottom-left{
        background-color: #a64de9;
        color: white;
    }
    .top-left{
       .line, h3{
        position: relative;
        left: 5vw;
        top: 1vh;
        }
    }
   
   .about-img{
       margin-left: 20vw;
       margin-top: 5vh;
       width: 23vw;
       
   }
 .about-header,  .desc{
       width: 20vw;
       
       color:#a64de9;
       margin-left: 15vw;
       
   }
   .desc{
       height: 40vh;
       overflow-y:auto;
       font-size: 1.2rem;
   }
   .about-header{
       margin-top: 10vh;
       font-size: 2.2rem;
   }
}
</style>