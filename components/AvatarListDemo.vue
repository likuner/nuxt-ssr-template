<template>
  <h3>AvatarList</h3>
  <AvatarList :list="list" />
</template>
<script>
export default {
  data () {
    return {
      list: [
        {
          src: 'https://dev-file.iviewui.com/BbnuuEiM0QXNPHVCvb3E2AFrawIjCkqW/avatar',
          tip: '史蒂夫·乔布斯'
        },
        {
          src: 'https://dev-file.iviewui.com/zhj85zgAfEjChCNIKT1LQENUIOyOYCaX/avatar',
          tip: '斯蒂夫·沃兹尼亚克'
        },
        {
          src: 'https://dev-file.iviewui.com/TkH54UozsINlex15TAMI00GElsfsKSiC/avatar',
          tip: '乔纳森·伊夫'
        }
      ]
    }
  }
}
</script>
