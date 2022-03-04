<template>
  <div class="slider-three">
    <div
      class="slider-three__line"
      :style="{ 'margin-left': '-' + 100 * offset + '%' }"
    >
      <app-slider-item
        v-for="item in sliderItems"
        :key="item.id"
        :item="item"
      ></app-slider-item>
    </div>
    <ul class="slider-three__ul">
      <li
        class="slider-three__li"
        v-for="(pag, idx) in sliderItems"
        :key="pag.id"
        :idx="idx"
        @click="slider(idx)"
        :class="{'slider-three__active': this.offset === idx}"
      ></li>
    </ul>
    <img
      @click="prevSlider"
      src="../../assets/images/arrow-left.png"
      alt="arrow"
      class="arrow-left"
    />
    <img
      @click="nextSlider"
      src="../../assets/images/arrow-right.png"
      alt="arrow"
      class="arrow-right"
    />
  </div>
</template>

<script>
import AppSliderItem from "./AppSliderItem.vue";
export default {
  data() {
    return {
      offset: 0,
    };
  },
  methods: {
    prevSlider() {
      if (this.offset > 0) {
        this.offset--;
      }
    
    },
    nextSlider() {
      if (this.offset >= this.sliderItems.length - 1) {
        this.offset = 0;
      } else {
        this.offset++;
      }
     
    },
    slider(idx) {
      this.offset = idx;
    },
  },
  computed: {
    currentStep() {
      return this.idx === this.offset;
    },
  },

  props: ["sliderItems"],
  components: {
    AppSliderItem,
  },
};
</script>

<style lang="scss" scoped>
</style>