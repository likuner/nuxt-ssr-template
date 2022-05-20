<template>
  <h3>CountUp</h3>
  <p class="ivu-m"><strong>目标值：1234，持续时间：6秒</strong></p>
  <CountUp :end="1234" :duration="6" ref="count" v-font="24" />
  <p class="ivu-m"><strong>控制</strong></p>
  <Button @click="handlePause">暂停/继续</Button>
  <Button @click="handleReset">重置</Button>
  <Button @click="handleStart">开始</Button>
  <Button @click="handleUpdate">更新至：</Button>
  <InputNumber v-model="update" :min="1" :max="10000" />
</template>
<script>
export default {
  data () {
    return {
      update: 5000
    }
  },
  methods: {
    handlePause () {
      this.$refs.count.CountUp.pauseResume();
    },
    handleReset () {
      this.$refs.count.CountUp.reset();
    },
    handleStart () {
      this.$refs.count.CountUp.start();
    },
    handleUpdate () {
      this.$refs.count.CountUp.update(this.update);
    },
  }
}
</script>
