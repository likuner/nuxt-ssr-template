<template>
  <h3>Split</h3>
  <div class="demo-split">
    <Split v-model="split">
      <template #left>
        <div class="demo-split-pane">
          Left Pane
        </div>
      </template>
      <template #right>
        <div class="demo-split-pane">
          Right Pane
        </div>
      </template>
    </Split>
  </div>
</template>
<script>
export default {
  data () {
    return {
      split: 0.5
    }
  },
}
</script>
<style>
.demo-split{
  height: 200px;
  border: 1px solid #dcdee2;
}
.demo-split-pane{
  padding: 10px;
}
</style>
