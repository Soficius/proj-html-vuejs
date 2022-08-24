<template>
  <div>
    <MyHeader :socials="socials" :navItems="navItems" logo="img/classic_shop_logo2x.png"/>
    <MyMain :featured="featured"/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
function navItem (text) {
  return { icon: 'fa-solid fa-angle-down', text }
}
export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },
  data: function () {
    return {
      socials: ['fa-brands fa-facebook-f', 'fa-brands fa-twitter', 'fa-brands fa-instagram', 'fa-brands fa-youtube'],
      navItems: [navItem('Home'), navItem('Shop'), navItem('Products'), navItem('Categories'), { text: 'News', icon: '' }, navItem('Elements')],
      featured: [
        { img: 'img/black_elegant_leather_jacket-200x260.jpg', title: 'Black Leather Jacket', tags: 'Man, Jackets, Jeans', oldPrice: 235, newPrice: 200 },
        { img: 'img/black_leather_suit-200x260.jpg', title: 'Black Leather Jacket', tags: 'Man, Jackets, Jeans', newPrice: 200 },
        { img: 'img/blue_jacket_and_white_stripe_tee-200x260.jpg', title: 'Black Leather Jacket', tags: 'Man, Jackets, Jeans', newPrice: 200 },
        { img: 'img/modern_black_leather_suit-200x260.jpg', title: 'Black Leather Jacket', tags: 'Man, Jackets, Jeans', newPrice: 200 }
      ]
    }
  }

}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
