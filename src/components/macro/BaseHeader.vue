<template>
  <header class="container-fluid">
    <SpotifyLogo id="logo"/>
  </header>
</template>

<script>
import SpotifyLogo from '../commons/SpotifyLogo.vue'
export default {
    name: 'BaseHeader',
    components:{
        SpotifyLogo
    }
}
</script>

<style lang="scss" scoped>
    header{
        height: 4.6875rem;
        background-color: var(--primary-color);
        display: flex;
        align-items: center;
    }

    #logo{
        height: 3.75rem;
    }
</style>