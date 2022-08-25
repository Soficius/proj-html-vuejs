<template>
    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item" v-for="(social,i) in socials" :key="'social-'+i">
            <a class="nav-link" href="#"><font-awesome-icon :icon="social" /></a>
        </li>
    </ul>
</template>

<script>
export default {
  name: 'SocialsBar',
  props: ['socials']
}
</script>
