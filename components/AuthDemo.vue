<template>
  <h3>Auth</h3>
  <div>
    <Divider>鉴权通过</Divider>
    <Auth authority="admin" access="admin">
      <Alert type="success">权限通过时显示</Alert>
      <template #noMatch>
        <Alert type="error">权限不通过时显示</Alert>
      </template>
    </Auth>
    <Divider>鉴权不通过</Divider>
    <Auth authority="admin" access="user">
      <Alert type="success">权限通过时显示</Alert>
      <template #noMatch>
        <Alert type="error">权限不通过时显示</Alert>
      </template>
    </Auth>
  </div>
</template>
<script>
export default {

}
</script>
