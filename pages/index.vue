<template>
  <div>
      <nuxt-link to="/login"> <div>Index</div> </nuxt-link>

      <input type="text"></input>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      show: 0,
    }
  },
  mounted() {
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>

</style>
