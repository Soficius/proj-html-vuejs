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
        <figure class="d-flex justify-content-center">
          <div class="d-flex flex-column">
            <img src="img/black_elegant_leather_jacket-200x260.jpg" alt="">
            <span><strong>Black leather jacket</strong></span>
            <span></span>
            <span></span>

          </div>
          <img src="img/black_leather_suit-200x260.jpg" alt="">
          <img src="img/blue_jacket_and_white_stripe_tee-200x260.jpg" alt="">
          <img src="img/modern_black_leather_suit-200x260.jpg" alt="">
        </figure>
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
  </div>
</template>

<script>
import JumboTron from './JumboTron.vue'
export default {
  name: 'MyMain',
  components: { JumboTron }
}
</script>
<style lang="scss">
@import '../assets/scss/vars.scss';
.man-testimonial{
  width: 6em;
}
</style>
