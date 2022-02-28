<template>
  <div>
    <img :src="require('../../assets/imges/slider-1/' + item.img)" alt="" />
  </div>
</template>

<script>
export default {
  props: ['item']
}
</script>

<style lang="scss" scoped>
</style>
