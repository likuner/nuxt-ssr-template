<template>
  <h3>Transfer</h3>
  <Transfer
    :data="data"
    :target-keys="targetKeys"
    :render-format="render"
    @on-change="handleChange"></Transfer>
</template>
<script>
export default {
  data () {
    return {
      data: this.getMockData(),
      targetKeys: this.getTargetKeys()
    }
  },
  methods: {
    getMockData () {
      let mockData = [];
      for (let i = 1; i <= 20; i++) {
        mockData.push({
          key: i.toString(),
          label: 'Content ' + i,
          description: 'The desc of content  ' + i,
          disabled: Math.random() * 3 < 1
        });
      }
      return mockData;
    },
    getTargetKeys () {
      return this.getMockData()
      .filter(() => Math.random() * 2 > 1)
      .map(item => item.key);
    },
    render (item) {
      return item.label;
    },
    handleChange (newTargetKeys, direction, moveKeys) {
      console.log(newTargetKeys);
      console.log(direction);
      console.log(moveKeys);
      this.targetKeys = newTargetKeys;
    }
  }
}
</script>
