<template>
  <h3>Login</h3>
  <div class="demo-login">
    <Login @on-submit="handleSubmit">
      <Mobile name="mobile" />
      <Captcha name="captcha" :field="['mobile']" @on-get-captcha="handleGetCaptcha" />
      <Submit />
    </Login>
  </div>
</template>
<script>
export default {
  methods: {
    handleSubmit (valid, { mobile, captcha }) {
      if (valid) {
        this.$Modal.info({
          title: '输入的内容如下：',
          content: 'mobile: ' + mobile + ' | captcha: ' + captcha
        });
      }
    },
    handleGetCaptcha () {
      this.$Message.info('获取验证码');
    }
  }
}
</script>
<style>
.demo-login{
  width: 400px !important;
  margin: 0 auto;
}
</style>
