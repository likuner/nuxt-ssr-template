<template>
  <h3>PageHeader</h3>
  <PageHeader :breadcrumb-list="breadcrumbList">
    <template #title><div class="demo-title">Title</div></template>
    <template #logo><div class="demo-logo">Logo</div></template>
    <template #content><div class="demo-content">Content</div></template>
    <template #extra><div class="demo-extra">Extra</div></template>
    <template #action><div class="demo-action">Action</div></template>
  </PageHeader>
</template>
<script>
export default {
  data () {
    return {
      breadcrumbList: [
        {
          title: '面包屑'
        }
      ]
    }
  }
}
</script>
<style>
.demo-title{
  background: #2b85e4;
}
.demo-logo{
  background: #2d8cf0;
}
.demo-content, .demo-action, .demo-extra{
  background: #2baee9;
}
</style>
