<template>
  <h2>test teleport</h2>

  <!-- <button type="primary" @click="disabled = !disabled">Click</button>
  <teleport to="body" :disabled="disabled">
    <span style="position: fixed">disabled: {{ disabled }}</span>
  </teleport> -->
  
  <div class="test">
    <el-tooltip
      :teleported="false"
      append-to="body"
      class="box-item"
      effect="dark"
      content="Top Left prompts info"
      placement="right"
    ><el-button>teleported="false", append-to="body, wrapped by div"</el-button></el-tooltip>
  </div>
</template>

<script setup>
// import { ref } from 'vue'
// const disabled = ref(true)
</script>

<style scoped>
</style>