<template>
  <h3>Tag</h3>
  <Tag>标签一</Tag>
  <Tag>标签二</Tag>
  <Tag v-if="show" closable @on-close="handleClose">标签三</Tag>
</template>
<script>
export default {
  data () {
    return {
      show: true
    }
  },
  methods: {
    handleClose () {
      this.show = false;
    }
  }
}
</script>
