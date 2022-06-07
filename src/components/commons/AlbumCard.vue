<template>
  <div class="album_card text-center">
      <img class="img-fluid" :src="album.poster" :alt="album.author">
      <h2 class="text-white text-uppercase">{{album.title}}</h2>
      <h5>{{album.author}}</h5>
      <small>{{album.year}}</small>
  </div>
</template>

<script>
export default {
    name:'AlbumCard',
    props: {
        album: Object,
    } 
}
</script>

<style lang="scss" scoped>
    .album_card{
        background-color: var(--primary-color);
        padding: .625rem;
        padding-bottom: 1.875rem;

        h2{
            font-size: 1.25rem;
        }

        h5, small{
            color: var(--text-gray);
        }
    }
</style>