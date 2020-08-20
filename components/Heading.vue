<template>
  <div id="fix-head" class="heading">
    <h3>{{pageTitle}}</h3>
    <div class="line"></div>
  </div>
</template>

<script>
export default {
  props: ['pageTitle'],
  data() {
    return {
      name: 'Kyle',
    }
  },
}
</script>

<style lang="scss">
#fix-head{
  position: fixed;
  top: 5vh;
  left: 3vw;
}
.heading {
  color: #a64de9;
  h3 {
    font-size: 2.2rem;
    font-weight: normal;
  }
}
.line {
  background-color: #a64de9;
  height: 5px;
  border-radius: 10px;
  width: 90px;
}
</style>