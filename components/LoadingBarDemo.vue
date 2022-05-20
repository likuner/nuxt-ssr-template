<template>
  <h3>LoadingBar</h3>
  <Button @click="start">Start</Button>
  <Button @click="finish">Finish</Button>
  <Button @click="error">Error</Button>
</template>
<script>
export default {
  methods: {
    start () {
      this.$Loading.start();
    },
    finish () {
      this.$Loading.finish();
    },
    error () {
      this.$Loading.error();
    }
  }
}
</script>
