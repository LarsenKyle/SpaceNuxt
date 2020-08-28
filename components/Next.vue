<template>
  <v-icon @click="showNext" id="right-mid">mdi-chevron-right</v-icon>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {
    showNext() {
      this.$emit('clicked', 1)
    },
  },
}
</script>

<style lang="scss">
#right-mid {
  position: fixed;
  top: 40vh;
  right: 7vw;
  color: $primary;
  font-size: 6rem;
}
</style>