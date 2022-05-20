<template>
  <h3>Progress</h3>
  <Progress :percent="25" :stroke-width="20" text-inside />
  <Progress :percent="45" :stroke-width="20" status="active" text-inside />
  <Progress :percent="65" :stroke-width="20" status="wrong" text-inside />
  <Progress :percent="100" :stroke-width="20" text-inside />
</template>
<script>
export default {

}
</script>
