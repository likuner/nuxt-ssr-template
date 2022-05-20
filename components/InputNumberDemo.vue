<template>
  <h3>InputNumber</h3>
  <InputNumber :max="10" :min="1" v-model="value"></InputNumber>
</template>
<script>
export default {
  data () {
    return {
      value: 1
    }
  }
}
</script>
