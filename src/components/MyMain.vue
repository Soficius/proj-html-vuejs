<template>
  <div>
    <!-- jumbotron copertina -->
    <JumboTron
      background="img/home1_slide_three_bg_2.jpg"
      height="520px"
      align="center"
      justify="center"
      color="white"
    >
      <div class="d-flex flex-column justify-content-center text-center">
          <h1>Brand New Arrivals</h1>
          <h5>New collection from New York</h5>
          <div class="d-flex flex-row justify-content-center align-items-center">
            <button class="rounded-pill bg-transparent me-4 p-2  border border-white"><a href="#" class="text-decoration-none text-white">View All</a></button>
            <button class="rounded-pill bg-transparent p-2 border border-white"><a href="#" class="text-decoration-none text-white">LookBook</a></button>
          </div>
      </div>
    </JumboTron>
    <!-- products sections -->
    <div class=" container text-center py-5">
      <h4>Featured Products</h4>
      <p>Must have products from our top sellers </p>
      <div class="d-flex justify-content-center">
        <div class="btn-group pb-3">
          <a href="#" class="btn btn-white active px-5" aria-current="page">Man</a>
          <a href="#" class="btn bg-l-gray px-5">Woman</a>
          <a href="#" class="btn bg-l-gray px-5">Accessories</a>
        </div>
      </div>
      <!-- images products section -->
      <div class="d-flex justify-content-center">
        <figure v-for="(item,i) in featured" :key="'featured-'+i">
          <div class="d-flex flex-column pe-3 text-start">
            <img :src="item.img" :alt="item.title" style="height:260px;width:200px">
            <h5>{{item.title}}</h5>
            <p>{{item.tags}}</p>
            <p>
              <span v-if="item.oldPrice"><del>{{item.oldPrice}}€</del></span>
              &nbsp;&nbsp;
              <span>{{item.newPrice}}€</span>
            </p>
          </div>
        </figure>
      </div>
    </div>
    <div class="d-flex">

      <!-- season collection section -->
      <JumboTron
      background="img/winter_collection_bg.jpg"
      height="500px"
      align="end"
      justify="center"
      bpos="top center"
      class="pb-5"
      >
         <div class="d-flex flex-column justify-content-center align-items-center text-center text-white">
          <h2>Winter Collection</h2>
          <span>STYLISH AND WARN</span>
          <button class="rounded-pill bg-transparent me-4 p-2  border border-white"><a href="#" class="text-decoration-none text-white">View more</a></button>
      </div>

      </JumboTron>
      <JumboTron
      background="img/spring_collection_bg.jpg"
      height="500px"
      align="end"
      justify="center"
      bpos="top center"
      class="pb-5"
      >
       <div class="d-flex flex-column justify-content-center align-items-center text-center text-white">
          <h2>Spring Collection</h2>
          <span>BRIGHT AND COLORFUL</span>
          <button class="rounded-pill bg-transparent me-4 p-2 border border-white"><a href="#" class="text-decoration-none text-white">View more</a></button>
      </div>
      </JumboTron>
      <JumboTron
      background="img/autumn_collection_bg.jpg"
      height="500px"
      align="end"
      justify="center"
      bpos="top center"
      class="pb-5"
      >
        <div class="d-flex flex-column justify-content-center align-items-center text-center text-white">
          <h2>Autumn Collection</h2>
          <span>RICH AND CONFORTABLE</span>
          <button class="rounded-pill bg-transparent me-4 p-2 border border-white"><a href="#" class="text-decoration-none text-white">View more</a></button>
      </div>
      </JumboTron>
    </div>

    <div>separooooooooooooooooo</div>
    <!--  offers section-->
    <JumboTron
    background="img/bkgd_confetti-compressor.jpg"
    height="520px"
    align="center"
    justify="center"
    >
      <div class="container w-75 d-flex">
        <JumboTron
        background="img/promo_box_1_bg.jpg"
        height="300px"
        align="center"
        class="me-4"
        color="white"
        >
          <div class="d-flex flex-column ps-5">
            <h1>70% Off</h1>
            <span>Vivamus tempor leo lacus, feugiat</span>
            <span>ut magna aliquam erat.</span>
            <button class="rounded-pill bg-transparent me-4 p-1 mt-1 border border-white border-2"><a href="#" class="text-decoration-none text-white">View more</a></button>
          </div>
        </JumboTron>
        <JumboTron
        background="img/promo_box_2_bg.jpg"
        height="300px"
         align="center"
        class="me-4"
        color="white"
        >
           <div class="d-flex flex-column ps-5">
            <h1>Free Shipping</h1>
            <span>Vivamus tempor leo lacus, feugiat</span>
            <span>ut magna aliquam erat.</span>
            <button class="rounded-pill bg-transparent me-4 p-1 mt-1 border border-white border-2"><a href="#" class="text-decoration-none text-white">View more</a></button>
          </div>
        </JumboTron>
      </div>
    </JumboTron>

    <!--  testimonials section -->
    <div>separooooooooooooooooo</div>
     <JumboTron
      background="img/testimonials_home_1_bg.jpg"
      height="520px"
      align="center"
      justify="center"
      color="white"
    >
      <div class="d-flex flex-column justify-content-center align-items-center text-center w-50">
        <img src="img/man_testimonial.png" alt="testimonial-man" class="man-testimonial">
         <p>Curabitur non tristique tortor. Vestibulum aliquet suscipit ipsum in volutpat. Donec vel lacinia sem, vitae semper nulla. In hac habitasse platea dictumst. Mauris consectetur est et nibh sadip hendrerit bibendum.</p>
         <p>Darío Pineda, Theme Fusion</p>
      </div>
    </JumboTron>
    <!-- blogs section -->
    <div class="container text-center py-5">
      <h1>From Our Blog</h1>
      <p>The Latest Classic Shop News</p>
    </div>
    <div class="d-flex justify-content-center container pb-5" >
      <div v-for="(blog,i) in blogs" :key="'blogs-'+i" class="d-flex flex-column pe-5" >
        <img :src="blog.img" :alt="blog.title">
        <h5>{{blog.title}}</h5>
        <p>{{blog.data}} | {{blog.comments.length}} Comments</p>
        <p>{{blog.description}}</p>
    </div>
    </div>
    <!-- section review -->
    <div class="container d-flex flex-row border-top border-1 py-5">
      <div class="container d-flex flex-column my-width">
        <h5>Featured</h5>
        <div class="d-flex flex-row my-height w-100 justify-content-between border-1 border-bottom pb-3" v-for="(item,i) in reviewFeaturedItems" :key="'rfi-'+i">
          <p>
            <span>{{item.description}}</span>
            <span v-if="item.stars"><RateReview class="w-100 d-block" :rate="item.stars"/></span>
            <span v-if="item.oldPrice"><del>{{item.oldPrice}}€</del></span>
            &nbsp;&nbsp;
            <span>{{item.newPrice}}€</span>
          </p>
          <img :src="item.img" :alt="item.description" class="h-100">
        </div>
      </div>
      <div class="container d-flex flex-column  my-width">
        <h5>On Sale</h5>
        <div class="d-flex flex-row my-height w-100 justify-content-between border-1 border-bottom pb-3" v-for="(item,i) in reviewSaleItems" :key="'rsi-'+i">
          <p>
            <span>{{item.description}}</span>
            <span v-if="item.stars"><RateReview class="w-100 d-block" :rate="item.stars"/></span>
            &nbsp;
            <span v-if="item.oldPrice"><del>{{item.oldPrice}}€</del></span>
            &nbsp;&nbsp;
            <span>{{item.newPrice}}€</span>
          </p>
          <img :src="item.img" :alt="item.description" class="h-100">
        </div>
      </div>
      <div class="container d-flex flex-column  my-width">
        <h5>Top Rated</h5>
        <div class="d-flex flex-row my-height w-100 justify-content-between border-1 border-bottom pb-3" v-for="(item,i) in reviewRateItems" :key="'rri-'+i">
          <p>
            <span>{{item.description}}</span>
            <span v-if="item.stars"><RateReview class="w-100 d-block" :rate="item.stars"/></span>
            <span v-if="item.oldPrice"><del>{{item.oldPrice}}€</del></span>
            &nbsp;&nbsp;
            <span>{{item.newPrice}}€</span>
          </p>
          <img :src="item.img" :alt="item.description" class="h-100">
        </div>
      </div>
      <div class="container d-flex flex-column  my-width">
            <h5>Latest Review</h5>
            <div class="d-flex flex-row my-height w-100 justify-content-between border-1 border-bottom pb-3" v-for="(item,i) in reviewLatestItems" :key="'rli-'+i">
                <p>
                <span>{{item.description}}</span>
                <span v-if="item.stars"><RateReview class="w-100 d-block" :rate="item.stars"/></span>
                <span v-if="item.oldPrice"><del>{{item.oldPrice}}€</del></span>
                &nbsp;&nbsp;
                <span>{{item.newPrice}}€</span>
              </p>
              <img :src="item.img" :alt="item.description" class="h-100">
            </div>
      </div>
    </div>
    <!-- brand logos -->
    <div class="container-fluid text-center bg-color-gray py-4">
      <h5 class="py-4">Brand Logos</h5>
      <div class="d-flex container justify-content-around">
        <img v-for="(logo,i) in logos" :key="'logos-'+i" :src="logo" alt="">
      </div>
    </div>
  </div>
</template>
<script>
import JumboTron from './JumboTron.vue'
import RateReview from './RateReview.vue'
export default {
  name: 'MyMain',
  components: { JumboTron, RateReview },
  props: ['featured', 'blogs', 'reviewFeaturedItems', 'logos', 'reviewSaleItems', 'reviewRateItems', 'reviewLatestItems']
}
</script>
<style lang="scss">
@import '../assets/scss/vars.scss';
.man-testimonial{
  width: 6em;
}
.my-width{
  width: calc(100%/4);
}
.bg-color-gray{
background-color: $color_light;
}
.my-height{
  height: 6em;
}
</style>
