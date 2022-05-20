<template>
  <h3>WordCount</h3>
  <div>
    <Input v-model="value" type="textarea" />
    <WordCount :value="value" :total="10" />
  </div>
</template>
<script>
export default {
  data () {
    return {
      value: ''
    }
  }
}
</script>
