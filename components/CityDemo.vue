<template>
  <h3>City</h3>
  <Row>
    <Col span="12">
      <City v-model="value1" />
    </Col>
    <Col span="12">
      <City v-model="value2" show-suffix />
    </Col>
  </Row>
</template>
<script>
export default {
  data () {
    return {
      value1: '110000',
      value2: '110000'
    }
  }
}
</script>
