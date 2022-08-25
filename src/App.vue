<template>
  <div>
    <MyHeader :socials="socials" :navItems="navItems" logo="img/classic_shop_logo2x.png"/>
    <MyMain :featured="featured" :blogs="blogs"
    :reviewFeaturedItems="reviewFeaturedItems"
    :logos="logos" :reviewSaleItems="reviewSaleItems"
    :reviewRateItems="reviewRateItems" :reviewLatestItems=" reviewLatestItems"/>
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
      ],
      blogs: [
        { img: 'img/post_img_12-320x202.jpg', title: 'Aenean lobortis sapien enim viverra', data: 'September 9th, 2015', description: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,', comments: [] },
        { img: 'img/post_img_11-320x202.jpg', title: 'Duis ac massa semper maximus', data: 'September 9th, 2015', description: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,', comments: [] },
        { img: 'img/post_img_10-320x202.jpg', title: 'Nunc fermint nulla eu justo sem id', data: 'September 9th, 2015', description: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,', comments: [] }
      ],
      reviewFeaturedItems: [
        { img: 'img/black_leather_jacket-120x156.jpg', description: 'Black Jacket', newPrice: 125 },
        { img: 'img/black_elegant_leather_jacket-120x156.jpg', description: 'Black Leather Jacket', newPrice: 200, oldPrice: 235, stars: 5 },
        { img: 'img/hipster_black_top-120x156.jpg', description: 'Hipster Black Top', newPrice: 57 }
      ],
      reviewSaleItems: [
        { img: 'img/black_leather_jacket-120x156.jpg', description: 'Black Jacket', newPrice: 125 },
        { img: 'img/black_elegant_leather_jacket-120x156.jpg', description: 'Black Leather Jacket', newPrice: 200, oldPrice: 235, stars: 5 },
        { img: 'img/hipster_black_top-120x156.jpg', description: 'Hipster Black Top', newPrice: 57 }
      ],
      reviewRateItems: [
        { img: 'img/black_leather_jacket-120x156.jpg', description: 'Black Jacket', newPrice: 125 },
        { img: 'img/black_elegant_leather_jacket-120x156.jpg', description: 'Black Leather Jacket', newPrice: 200, oldPrice: 235, stars: 5 },
        { img: 'img/hipster_black_top-120x156.jpg', description: 'Hipster Black Top', newPrice: 57 }
      ],
      reviewLatestItems: [
        { img: 'img/black_leather_jacket-120x156.jpg', description: 'Black Jacket', newPrice: 125 },
        { img: 'img/black_elegant_leather_jacket-120x156.jpg', description: 'Black Leather Jacket', newPrice: 200, oldPrice: 235, stars: 5 },
        { img: 'img/hipster_black_top-120x156.jpg', description: 'Hipster Black Top', newPrice: 57 }
      ],
      logos: ['img/b_logotype_6.png', 'img/b_logotype_7.png', 'img/b_logotype_1.png', 'img/b_logotype_2.png', 'img/b_logotype_3.png']
    }
  }

}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
