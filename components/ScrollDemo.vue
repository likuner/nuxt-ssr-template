<template>
  <h3>Scroll</h3>
  <Scroll :on-reach-bottom="handleReachBottom">
    <Card dis-hover v-for="(item, index) in list" :key="index" style="margin: 32px 0">
      Content {{ item }}
    </Card>
  </Scroll>
</template>
<script>
export default {
  data () {
    return {
      list: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    }
  },
  methods: {
    handleReachBottom () {
      return new Promise(resolve => {
        setTimeout(() => {
          const last = this.list[this.list.length - 1];
          for (let i = 1; i < 11; i++) {
            this.list.push(last + i);
          }
          resolve();
        }, 2000);
      });
    }
  }
}
</script>
