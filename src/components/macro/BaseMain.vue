<template>
  <main>
      <div class="container">
          <div class="row">
              <div class="col-12 col-md-4 col-lg-2">
                <AlbumCard/>
              </div>
          </div>
      </div>
  </main>
</template>

<script>
import AlbumCard from '../../components/commons/AlbumCard'

export default {
    name: 'BaseMain',
    components:{
        AlbumCard,
    },
    
}
</script>

<style lang="scss" scoped>
    main{
        padding: 50px 0;
        min-height: 100vh;
        background-color: var(--secondary-color);

        .row{
            margin: auto;
            row-gap: 1.25rem;
        }
    }
</style>