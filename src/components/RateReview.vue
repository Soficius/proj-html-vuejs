<template>
<span>
  <span v-for="n in 5" :key="'s'-n" :class="n <= rate ? 'e-primary' : 'e-white'">★</span>
</span>
</template>

<script>
export default {
  name: 'RateReview',
  props: ['rate']
}
</script>

<style lang="scss">
@import '../assets/scss/vars.scss';
.e-primary{
    color: transparent;
    text-shadow: 0 0 0 $color_primary;
}
.e-white{
    color: transparent;
    text-shadow: 0 0 0 white;
}
</style>
