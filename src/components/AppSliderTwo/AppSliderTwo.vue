<template>
  <div class="container-two">
    <div
      class="slider-two"
      :style="{ 'margin-left': '-' + 100 * offset + '%' }"
    >
      <app-slider-item
        v-for="(item, idx) in sliderItems"
        :key="item"
        :item="item"
      ></app-slider-item>
    </div>
    <ul class="slider-two__ul">
      <li
        class="slider-two__li"
        v-for="(pag, idx) in sliderItems"
       :class="{'slider-two__active': this.offset === idx}"
        :key="pag"
        :idx="idx"
         @click="slider(idx)"
      ></li>
    </ul>
  </div>
</template>

<script>
import AppSliderItem from "./AppSliderItem.vue";
export default {
  data() {
    return {
      activeIndex: 0,
      offset: 0,
    };
  },
  methods: {
    slider(idx) {
      this.offset = idx;
      console.log(this.offset);
    },
  },
  props: ["sliderItems"],
  components: { AppSliderItem },
};
</script>

<style lang="scss" scoped>
</style>
