<template>
  <h3>Drawer</h3>
  <Button @click="value = true" type="primary">Open</Button>
  <Drawer title="Basic Drawer" :closable="false" v-model="value">
    <p>Some contents...</p>
    <p>Some contents...</p>
    <p>Some contents...</p>
  </Drawer>
</template>
<script>
export default {
  data () {
    return {
      value: false
    }
  }
}
</script>
