<template>
  <div class="container-fluid jumbotron" :style="jumboStyle">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'JumboTron',
  props: ['background', 'height', 'align', 'justify', 'color', 'bpos'],
  computed: {
    jumboStyle () {
      return {
        backgroundImage: 'url(' + this.background + ')',
        height: this.height || '200px',
        alignItems: this.align || '',
        justifyContent: this.justify || '',
        color: this.color || '',
        backgroundPosition: this.bpos || 'center'
      }
    }
  }
}
</script>

<style scoped>
  .jumbotron{
    display: flex;
    background-repeat: no-repeat;
    background-size: cover;
  }
</style>
