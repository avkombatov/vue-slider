<template>
    
  <img class="slider__img" :src="require('../../assets/images/slider-2/' + item.img)" alt="" />
    
</template>

<script>
export default {
  props: ['item']
}
</script>

<style lang="scss" scoped>

</style>
