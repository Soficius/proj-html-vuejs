<template>
    <ul :class="ul">
        <li :class="li" v-for="(social,i) in socials" :key="'social-'+i">
            <a v-if="nav" class="nav-link" href="#"><font-awesome-icon :icon="social" /></a>
            <font-awesome-icon v-else :icon="social" />
        </li>
    </ul>
</template>

<script>
export default {
  name: 'SocialsBar',
  props: { socials: Array, nav: Boolean },
  computed: {
    ul () { return this.nav ? 'navbar-nav me-auto mb-2 mb-lg-0' : 'list-inline' },
    li () { return this.nav ? 'nav-item' : 'list-inline-item' },
    a () { return this.nav ? 'nav-link' : '' }
  }
}
</script>
