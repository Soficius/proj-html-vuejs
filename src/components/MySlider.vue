<template>
  <div class="d-flex position-relative">
    <div class="d-flex position-absolute a-left align-items-center">
      <button class="btn btn-secondary" style="height:6em;" @click.prevent="scrollLeft">&lt;</button>
    </div>
    <div class="d-flex overflow-hidden" ref="slider">
      <div v-for="(image,i) in images" :key="'msi-'+i">
        <img :src="image" style="height:24em"/>
      </div>
    </div>
    <div class="d-flex position-absolute a-right align-items-center">
      <button class="btn btn-secondary" style="height:6em;" @click.prevent="scrollRight">></button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MySlider',
  props: { images: Array },
  methods: {
    scrollRight () {
      this.$refs.slider.scrollTo({ left: this.$refs.slider.scrollLeft + this.$refs.slider.clientWidth, behavior: 'smooth' })
    },
    scrollLeft () {
      this.$refs.slider.scrollTo({ left: this.$refs.slider.scrollLeft - this.$refs.slider.clientWidth, behavior: 'smooth' })
    }
  }
}
</script>

<style>
.a-left{
  top:0;
  bottom:0;
  left:0;
}
.a-right{
  top:0;
  bottom:0;
  right:0;
}
</style>
