<template>
  <div>
    <MyHeader :socials="socials" :navItems="navItems" logo="img/classic_shop_logo2x.png"/>
    <MyMain :featured="featured" :blogs="blogs"
    :reviewFeaturedItems="reviewFeaturedItems"
    :bestSellersImgs="bestSellersImgs"
    :logos="logos" :reviewSaleItems="reviewSaleItems"
    :reviewRateItems="reviewRateItems" :reviewLatestItems=" reviewLatestItems"/>
    <MyFooter
    :socials="socials" :topProducts="topProducts"
    :recentPost="recentPost" :tags="tags"/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import MyFooter from './components/MyFooter.vue'
function navItem (text) {
  return { icon: 'fa-solid fa-angle-down', text }
}
export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter
  },
  data: function () {
    return {
      socials: ['fa-brands fa-facebook-f', 'fa-brands fa-twitter', 'fa-brands fa-instagram', 'fa-brands fa-youtube'],
      navItems: [navItem('Home'), navItem('Shop'), navItem('Products'), navItem('Categories'), { text: 'News', icon: '' }, navItem('Elements')],
      featured: [
        { img: 'img/black_elegant_leather_jacket-200x260.jpg', title: 'Black Leather Jacket', tags: 'Man, Jackets, Jeans', oldPrice: 235, newPrice: 200 },
        { img: 'img/black_leather_suit-200x260.jpg', title: 'Black Leather suit', tags: 'Man, Jackets', newPrice: 176 },
        { img: 'img/blue_jacket_and_white_stripe_tee-200x260.jpg', title: 'Blue Jacket & Stripe Tee', tags: 'Man, Jackets,Ssuits', newPrice: 200 },
        { img: 'img/modern_black_leather_suit-200x260.jpg', title: 'Modern Black Leather Suit', tags: 'Man, Jackets', newPrice: 96 }
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
        { img: 'img/black_elegant_leather_jacket-120x156.jpg', description: 'Black Leather Jacket', newPrice: 200, oldPrice: 235, stars: 5 },
        { img: 'img/blue_leather_jacket-120x156.jpg', description: 'Black Leather Jacket', newPrice: 80, oldPrice: 60 },
        { img: 'img/leather_gloves-120x156.jpg', description: 'Casual Colorful Gloves', newPrice: 24, oldPrice: 36 }
      ],
      reviewRateItems: [
        { img: 'img/leather_gloves-120x156.jpg', description: 'Casual Colorful Gloves', newPrice: 45, stars: 5 },
        { img: 'img/black_elegant_leather_jacket-120x156.jpg', description: 'Black Leather Jacket', newPrice: 200, oldPrice: 235, stars: 5 },
        { img: 'img/spring_printed_dress-120x156.jpg', description: 'Spring Printed Dress', newPrice: 47, stars: 5 }
      ],
      reviewLatestItems: [
        { img: 'img/black_elegant_leather_jacket-120x156.jpg', description: 'Black Leather Jacket', newPrice: 200, oldPrice: 235, stars: 5 },
        { img: 'img/leather_gloves-120x156.jpg', description: 'Casual Colorful Gloves', newPrice: 45, stars: 5 },
        { img: 'img/spring_printed_dress-120x156.jpg', description: 'Spring Printed Dress', newPrice: 47, stars: 5 }
      ],
      logos: ['img/b_logotype_6.png', 'img/b_logotype_7.png', 'img/b_logotype_1.png', 'img/b_logotype_2.png', 'img/b_logotype_3.png'],
      topProducts: [
        { img: 'img/leather_gloves-120x156.jpg', starts: '5', newPrice: '45', title: 'Leather Gloves' },
        { img: 'img/black_elegant_leather_jacket-120x156.jpg', starts: '5', newPrice: '200', oldPrice: '235', title: 'Black Leather Jacket' },
        { img: 'img/spring_printed_dress-120x156.jpg', title: 'Spring Printed Dress', newPrice: '47', starts: 5 }
      ],
      recentPost: [
        'Aenean lobortis sapien enim viverra',
        'Duis ac massa semper maximus',
        'Nuc fermint nulla eu justo sem id',
        'aliquam posuere magnaeget nibh',
        'Cras ac nulla ac consecte rutrum',
        'Fusce mattis nunc ut aliquam'
      ],
      tags: [
        'Black', 'boots', 'Brown', 'Casual', 'D&G',
        'Fabric', 'flowers', 'Grey', 'hat', 'Hipster',
        'lines', 'multi-purpose', 'New York', 'Outdoors',
        'red', 'responsive', 'summer', 'sweater', 'Travel',
        'Warm', 'White', 'Winter'
      ],
      bestSellersImgs: [
        'img/black_elegant_leather_jacket.jpg',
        'img/blue_jacket_and_white_stripe_tee.jpg',
        'img/blue_leather_jacket.jpg',
        'img/hipster_black_top.jpg',
        'img/modern_black_leather_suit.jpg',
        'img/modern_love_tee.jpg',
        'img/spring_printed_dress.jpg'
      ]
    }
  }

}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
