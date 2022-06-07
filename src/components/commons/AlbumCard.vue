<template>
  <div class="album_card text-center">
      <img class="img-fluid" src="http://via.placeholder.com/700x700" alt="Non va">
      <h2 class="text-white text-uppercase">New Jersey</h2>
      <h5>Bon Jovi</h5>
      <small>1988</small>
  </div>
</template>

<script>
export default {
    name:'AlbumCard'
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