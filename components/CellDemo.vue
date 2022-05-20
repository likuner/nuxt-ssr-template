<template>
  <h3>Cell</h3>
  <div style="padding: 10px;background: #f8f8f9">
    <Card title="Options" icon="ios-options" :padding="0" shadow style="width: 300px;">
      <CellGroup>
        <Cell title="Only show titles" />
        <Cell title="Display label content" label="label content" />
        <Cell title="Display right content" extra="details" />
        <Cell title="Disabled" disabled />
        <Cell title="Selected" selected />
        <Cell title="With Badge">
          <template #extra>
            <Badge :count="10" />
          </template>
        </Cell>
        <Cell title="With Switch">
          <template #extra>
            <Switch v-model="switchValue" />
          </template>
        </Cell>
      </CellGroup>
    </Card>
  </div>
</template>
<script>
export default {
  data () {
    return {
      switchValue: true
    }
  },
}
</script>
