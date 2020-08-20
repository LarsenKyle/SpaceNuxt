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
   </div>
</template>

<script>
export default {
data(){
    return{
        pageTitle: 'Explore My Work'
    }
},
props:["work"],
watch:{
  
}
}
</script>

<style>

</style>