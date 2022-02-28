<template>
  <app-slider-one :sliderItems="sliderItems" :interval="3000"></app-slider-one>
  <app-slider-two :sliderItems="sliderItems"></app-slider-two>
</template>

<script>
import AppSliderOne from './components/AppSliderOne/AppSliderOne.vue'
import AppSliderTwo from './components/AppSliderTwo/AppSliderTwo.vue'
export default {
  data () {
    return {
      sliderItems: [
        { id: 1, name: 'img-1', img: 'img-1.jpg', text: 'number-1' },
        { id: 2, name: 'img-2', img: 'img-2.jpg', text: 'number-2' },
        { id: 3, name: 'img-3', img: 'img-3.jpg', text: 'number-3' },
        { id: 4, name: 'img-4', img: 'img-4.jpg', text: 'number-4' },
        { id: 5, name: 'img-5', img: 'img-5.jpg', text: 'number-5' }
      ]
    }
  },
  components: { AppSliderOne, AppSliderTwo }
}
</script>

<style>
</style>
