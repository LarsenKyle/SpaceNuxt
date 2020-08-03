<template>
  <header class="header">
    <ul class="flex ml-auto mr-15 pr-5 mt-7">
      <li class="pa-2 pr-2 mr-16 ml-12">
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li class="pa-2 mr-16 ml-12">
        <nuxt-link to="/work">Work</nuxt-link>
      </li>
      <li class="pa-2 mr-16 ml-12">
        <nuxt-link to="/about">About</nuxt-link>
      </li>
      <li class="pa-2 mr-12 ml-12">
        <nuxt-link to="/about">Contact</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
}
</script>

<style lang="scss">
.header {
  margin-left: auto;
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
