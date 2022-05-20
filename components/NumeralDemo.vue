<template>
  <h3>Numeral</h3>
  <div>
    <p class="ivu-m"><strong>初始内容：$10,000.00</strong></p>
    <Numeral :value="value"></Numeral>
    <p class="ivu-m"><strong>操作</strong></p>
    <Button @click="handleChange">转换 value</Button>
  </div>
</template>
<script>
export default {
  data () {
    return {
      value: '$10,000.00'
    }
  },
  methods: {
    handleChange () {
      this.value = '$10,000.23';
    }
  }
}
</script>
