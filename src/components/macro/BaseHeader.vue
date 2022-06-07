<template>
  <header>
    <div class="container-fluid">
        <SpotifyLogo/>
    </div>
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
        height: 75px;
        background-color: var(--primary-color);
    }
</style>