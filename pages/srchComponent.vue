<template>
  <div>
    <p>Try to type something in the input field below.</p>
    <p>If this component called as the root, like /srchComponent, it will reinintialize after each key press.</p>
    <p>If this component wrapped in the nuxt-child, it will work as expected without constant reinitializations.</p>
    <input v-model="srch">
  </div>
</template>
<script>
export default {
  data () {
    return {
      srch: this.$route.query.srch
    }
  },
  watch: {
    srch (srch) {
      this.$router.push({name: this.$route.name, query: {srch}})
    }
  },
  created () {
    console.log('Component created:', this.$route.name)
  },
  beforeDestroy () {
    console.log('Component is about to be destroyed:', this.$route.name)
  }
}
</script>