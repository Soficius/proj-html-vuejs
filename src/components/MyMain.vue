<template>
  <div>
    <!-- jumbotron -->
    <JumboTron
      background="img/home1_slide_three_bg_2.jpg"
      height="420px"
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
  </div>
</template>

<script>
import JumboTron from './JumboTron.vue'
export default {
  name: 'MyMain',
  components: { JumboTron }
}
</script>
<style>
</style>
