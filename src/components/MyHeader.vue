<template>
<header>
    <nav class="navbar navbar-expand-lg navbar-light border-1 border-bottom">
    <div class="container">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item" v-for="(social,i) in socials" :key="'social-'+i">
            <a class="nav-link" href="#"><font-awesome-icon :icon="social" /></a>
            </li>
        </ul>
        <span class="navbar-text mr-3">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
            <a class="nav-link text-secondary" href="#">Shopping Cart</a>
            </li>
            <li class="nav-item border-end border-1 border-start">
            <a class="nav-link text-secondary" href="#">My Account</a>
            </li>
            <li class="nav-item">
            <a class="nav-link" href="#"><font-awesome-icon icon="fa-solid fa-cart-shopping" class="me-2"/>Cart</a>
            </li>
        </ul>
        </span>
        </div>
    </nav>
    <nav class="navbar navbar-light p-0">
  <div class="container height-c">
    <a class="navbar-brand" href="#">
      <img :src="logo" alt="" height="50">
    </a>
     <ul class="navbar-nav mb-2 mb-lg-0  flex-row h-100">
        <li @click="activeItem=i" :class="'nav-item pe-3 h-100 d-flex align-items-center'+(activeItem===i? ' active': '')" v-for="({icon,text},i) in navItems" :key="'items-'+i">
            <a class="nav-link" href="#">{{text}} <font-awesome-icon :icon="icon" /></a>
        </li>
        <li class="d-flex align-items-center"><a href="#" class="text-decoration-none text-white p-2 bg-primary rounded-pill">Shop Now</a></li>
    </ul>
  </div>

</nav>
</header>

</template>

<script>
export default {
  name: 'MyHeader',
  props: ['socials', 'logo', 'navItems'],
  data: function () {
    return { activeItem: 0 }
  }
}
</script>

<style>
.height-c{
    height: 100px;
}
.active{
 border-top: 2px solid blue
}
</style>
