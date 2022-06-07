<template>
  <section>
      <div class="container">
          <div class="row" v-if="albums.length == 10">
            <AlbumCard class="col-12 col-md-4 col-lg-2" v-for="album in albums" :album="album" :key="album"/>
          </div>
          <div v-else>
            <SpinnerLoading/>
          </div>
      </div>
  </section>
</template>

<script>
import AlbumCard from '../../components/commons/AlbumCard'
import SpinnerLoading from '../../components/commons/SpinnerLoading'
import axios from 'axios'

export default {
    name: 'AlbumSection',
    components:{
        AlbumCard,
        SpinnerLoading,
    },
    data(){
        return{
            albums: [],
        }
    },
    created(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response)=> {
            this.albums = response.data.response;
        })
        .catch((error)=> {
            console.log(error);
        })
    },
}
</script>

<style lang="scss" scoped>
    .row{
        gap: 1.25rem;
        justify-content: space-around;
    }
</style>