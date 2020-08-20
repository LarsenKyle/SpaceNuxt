<template>
 <div class="about-grid office">
      <div class="top-left office">
        <Heading :pageTitle="pageTitle" /> 
      </div>
      <div class="top-right office">
         <Nav />
        
      </div>
      <div class="bottom-left office">
          <img class="galaxy" src="../assets/explode.svg" alt="">
         
      </div>
      <div class="bottom-right office">
          <img class="out-img" src="../assets/hobbie.png" alt="Profile shot in Utah mountains">
           <img class="explode" src="../assets/galaxy.svg" alt="">
          
          <h2 class="about-header" >Out of Office</h2>
          <p class="desc">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam beatae omnis praesentium fugiat odit illum dolor aliquam explicabo nesciunt, nisi deserunt adipisci! Quam libero quia voluptates enim! Expedita, voluptates accusantium.</p>
      </div>
  </div>

</template>

<script>
import Heading from './Heading'
export default {
components:{
    Heading
},
data(){
    return{
        pageTitle: "Learn About Me"
    }
}
}
</script>

<style lang="scss">
.about-grid{
    .out-img{
        width: 23vw;
        position: fixed;
        left: 19vw;
        top: 25vh;
    }
    &.office{
      
        .desc, .about-header, a{
            color: white;
        }
    .heading{
        .line{
            background-color: $primary
        }
        h3{
            color: $primary
        }
    }
    .top-left, .bottom-left{
            background-color: white
            
       
    }
    .bottom-right, .top-right{
        background-color: $primary
    }
    }
}
</style>