<template>
  <div class="container-one">
    <div
      class="slider-one"
      :style="{ 'margin-left': '-' + 100 * offset + '%' }"
    >
      <app-slider-item
        v-for="item in sliderItems"
        :key="item.id"
        :item="item"
      ></app-slider-item>
    </div>
  </div>
  <div class="buttons-one">
    <button class="button-prev__one" @click="prevSlider">Prev</button>
    <button class="button-next__one" @click="nextSlider">Next</button>
  </div>
</template>

<script>
import AppSliderItem from './AppSliderItem.vue'
export default {
  data () {
    return {
      offset: 0
    }
  },
  methods: {
    prevSlider () {
      if (this.offset > 0) {
        this.offset--
      // console.log(this.offset)
      }
    },
    nextSlider () {
      if (this.offset >= this.sliderItems.length - 1) {
        this.offset = 0
      } else {
        this.offset++
      }

      // console.log(this.offset)
    }

  },
  mounted () {
    if (this.interval > 0) {
      const vm = this
      setInterval(function () {
        vm.nextSlider()
      }, vm.interval)
    }
  },
  props: ['sliderItems', 'interval'],
  components: { AppSliderItem }
}
</script>

<style lang="scss" scoped>
</style>
