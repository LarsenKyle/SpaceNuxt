<template>
  <header class="header">
    <ul class="flex ml-auto mr-15 pr-5 mt-7">
      <li v-bind:class="{ active: home}" class="pa-2 pr-2 mr-16 ml-12">
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li v-bind:class="{ active: work}" class="pa-2 mr-16 ml-12">
        <nuxt-link to="/work">Work</nuxt-link>
      </li>
      <li v-bind:class="{ active: about}" class="pa-2 mr-16 ml-12">
        <nuxt-link to="/about">About</nuxt-link>
      </li>
      <li v-bind:class="{ active: contact}" class="pa-2 mr-12 ml-12">
        <nuxt-link to="/contact">Contact</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data(){
    return{
      home: false,
      work: false,
      about: false,
      contact: false
    }
  },
  mounted(){
   
switch(this.$router.history.current.name){
  case "index":
    this.home = true;
    break;
  case "work": 
    this.work = true;
    break;
  case "about": 
    this.about = true;
    break;
  case "contact": 
    this.contact = true;
    break;

}

  }
}
</script>

<style lang="scss">
.header {
  position: fixed;
  top: 1vh;
  right: 1vh;
}
.active{
  border-top:#a64de9 solid 3px;
}
.flex {
  display: flex;
  text-decoration: none;

  list-style-type: none;
  a {
    font-size: 1.4rem;
    text-decoration: none;
    color: #a64de9;
    :visited {
      color: #a64de9;
    }
  }
}
</style>
