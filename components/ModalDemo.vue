<template>
  <h3>Modal</h3>
  <Button type="primary" @click="modal = true">Display dialog box</Button>
  <Modal
    v-model="modal"
    title="Common Modal dialog box title"
    @on-ok="ok"
    @on-cancel="cancel">
    <p>Content of dialog</p>
    <p>Content of dialog</p>
    <p>Content of dialog</p>
  </Modal>
</template>
<script>
export default {
  data () {
    return {
      modal: false
    }
  },
  methods: {
    ok () {
      this.$Message.info('Clicked ok');
    },
    cancel () {
      this.$Message.info('Clicked cancel');
    }
  }
}
</script>
