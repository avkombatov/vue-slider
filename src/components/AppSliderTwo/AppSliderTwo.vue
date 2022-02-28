<template>
  <div class="container-two">
    <div class="slider-two">
      <app-slider-item
        v-for="item in sliderItems"
        :key="item.id"
        :item="item"
      ></app-slider-item>

    </div>
     <ul class="slider-two__ul">
        <li class="slider-two__li" v-for="pag in sliderItems" :key="pag"></li>
      </ul>
  </div>
</template>

<script>
import AppSliderItem from './AppSliderItem.vue'
export default {
  props: ['sliderItems'],
  components: { AppSliderItem }
}
</script>

<style lang="scss" scoped>
</style>
