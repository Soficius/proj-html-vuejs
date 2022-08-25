<template>
  <div class=" text-white">
    <!-- subscribe section -->
    <div class="container-fluid my-height d-flex justify-content-center align-items-center c-color">
      <div class="d-flex justify-content-between w-75">
          <div  class="d-flex">
            <button class="btn btn-offers me-4">
              <font-awesome-icon icon="fa-solid fa-envelope" />
            </button>
            <h3 class="text-white">Subscribe now and get special offers</h3>
          </div>
          <form class="d-flex">
            <input class="me-2 rounded-pill" type="search" placeholder="Insert your mail" aria-label="Search">
            <button class="btn btn-success col-d-gray text-white rounded-pill m3-2" type="submit">Send</button>
           </form>
      </div>
    </div>
    <!-- section post/tags/generics -->
    <div class="container-fluid bg-c-color ">
      <div class="container d-flex py-4 my-width">
      <div class="container d-flex p-5">
        <div class="d-flex flex-column">
          <img src="img/classic_shop_logo_footer.png" class="pb-3" alt="">
          <div class="text-white">12345 North Main Street,</div>
          <div class="text-white">New York, NY 555555</div>
          <div class="text-white">Phone: 1.800.555.6789</div>
          <div class="text-white">Phone: 1.800.555.6789</div>
          <div class="text-white">Web: Theme-fusion.com</div>
          <SocialsBar :socials="socials" class="pt-3 text-white"/>
        </div>
      </div>
      <div class="container d-flex flex-column">
        <h5 class="py-5">TOP RATED PRODUCTS</h5>
        <div class="d-flex flex-row my-height w-100 justify-content-between border-1 border-bottom pb-3 text-white" v-for="(item,i) in topProducts" :key="'tp-'+i">
          <p>
            <span>{{item.title}}</span>
            <span v-if="item.stars"><RateReview class="w-100 d-block" :rate="item.stars"/></span>
            <span v-if="item.oldPrice"><del>{{item.oldPrice}}€</del></span>
            &nbsp;&nbsp;
            <span>{{item.newPrice}}€</span>
          </p>
          <img :src="item.img" :alt="item.title" class="h-100">
        </div>
      </div>
      <div class="container d-flex flex-column text-white">
        <h5 class="py-5">RECENT POST</h5>
         <div v-for="(post,i) in recentPost" :key="'recentPost-'+i" class="border-1 border-bottom py-2"  >
          <span>> {{post}}</span>
         </div>
      </div>
      <div class="container d-flex flex-column">
        <h5 class="py-5">TAGS</h5>
        <div class="container-fluid d-flex flex-wrap">
          <div v-for="(tag,i) in tags" :key="'tags-'+i" class="p-2"  >
            <button class="btn btn-outline-white rounded-0 text-white border-white">{{tag}}</button>
          </div>
        </div>
      </div>
    </div>
    </div>
    <!-- section payments -->
    <div class="container-fluid text-center bg-payments py-5">
      © Copyright 2012 - 2022 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress
    </div>
  </div>
</template>

<script>
import SocialsBar from './SocialsBar.vue'
import RateReview from './RateReview.vue'
export default {
  name: 'MyFooter',
  components: { SocialsBar, RateReview },
  props: ['socials', 'topProducts', 'recentPost', 'tags']
}
</script>

<style lang="scss">
@import '../assets/scss/vars.scss';
.c-color{
  background-color: $subcribe;
}
.bg-c-color{
  background-color: $special_offers ;
}
.bg-payments{
  background-color: $payments;
}
.btn-offers{
  --bs-btn-color: #fff !important;
  --bs-btn-bg: $special_offers !important;
  --bs-btn-border-color: #6c757d !important;
  --bs-btn-hover-color: #fff;
  --bs-btn-hover-bg: $special_offers;
  --bs-btn-hover-border-color: $special_offers;
  --bs-btn-focus-shadow-rgb: 130, 138, 145;
  --bs-btn-active-color: #fff;
  --bs-btn-active-bg: $special_offers;
  --bs-btn-active-border-color: $special_offers;
  --bs-btn-active-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  --bs-btn-disabled-color: #fff;
  --bs-btn-disabled-bg: #6c757d;
  --bs-btn-disabled-border-color: #6c757d;
  border-radius: 100% !important;
}
.col-d-gray{
  background-color: $color_primary !important;
  border-color: $color_primary !important;
}
.my-height{
  height: 200px;
}
.my-width{
  width: calc(100%/4);
}
.my-height{
  height: 6em;
}
</style>
