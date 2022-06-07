<template>
    <main>
        <AlbumSection/>
    </main>
</template>

<script>
import AlbumSection from '../../components/sections/AlbumSection'

export default {
    name: 'BaseMain',
    components:{
        AlbumSection,
    },
    
}
</script>

<style lang="scss" scoped>
    main{
         background-color: var(--secondary-color);
         padding: 50px 0;
         min-height: calc(100vh - 4.6875rem);
    }
</style>