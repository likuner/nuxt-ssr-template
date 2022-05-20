<template>
  <h3>TagSelect</h3>
  <TagSelect v-model="value">
    <TagSelectOption name="tag1">选项一</TagSelectOption>
    <TagSelectOption name="tag2">选项二</TagSelectOption>
    <TagSelectOption name="tag3">选项三</TagSelectOption>
    <TagSelectOption name="tag4">选项四</TagSelectOption>
    <TagSelectOption name="tag5">选项五</TagSelectOption>
    <TagSelectOption name="tag6">选项六</TagSelectOption>
  </TagSelect>
</template>
<script>
export default {
  data () {
    return {
      value: []
    }
  }
}
</script>
