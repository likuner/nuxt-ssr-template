<template>
  <h3>Rate</h3>
  <Rate allow-half v-model="valueHalf" />
</template>
<script>
export default {
  data () {
    return {
      valueHalf: 2.5
    }
  }
}
</script>
