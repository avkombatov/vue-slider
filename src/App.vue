<template>
  <app-slider-one :sliderItems="sliderItems" :interval="3000"></app-slider-one>
</template>

<script>
import AppSliderOne from './components/AppSliderOne/AppSliderOne.vue'
export default {
  data () {
    return {
      sliderItems: [
        { id: 1, name: 'img-1', img: 'img-1.jpg' },
        { id: 2, name: 'img-2', img: 'img-2.jpg' },
        { id: 3, name: 'img-3', img: 'img-3.jpg' },
        { id: 4, name: 'img-4', img: 'img-4.jpg' },
        { id: 5, name: 'img-5', img: 'img-5.jpg' }
      ]
    }
  },
  components: { AppSliderOne }
}
</script>

<style>
</style>
