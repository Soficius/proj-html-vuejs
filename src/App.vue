<template>
<MyHeader :socials="socials" :navItems="navItems" logo="img/classic_shop_logo2x.png"/>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
function navItem (text) {
  return { icon: 'fa-solid fa-angle-down', text }
}
export default {
  name: 'App',
  components: {
    MyHeader
  },
  data: function () {
    return {
      socials: ['fa-brands fa-facebook-f', 'fa-brands fa-twitter', 'fa-brands fa-instagram', 'fa-brands fa-youtube'],
      navItems: [navItem('Home'), navItem('Shop'), navItem('Products'), navItem('Categories'), { text: 'News', icon: '' }, navItem('Elements')]
    }
  }

}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
