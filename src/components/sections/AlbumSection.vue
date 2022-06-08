<template>
  <section>
      <div class="container">
          <SelectBar @sel="selectedGenr" />
          <div class="row row-cols-lg-5 g-3" v-if="albums.length == 10">
            <div class="col-12 col-md-4 col-lg" v-for="(album,index) in searchFilter" :key="index">
                <AlbumCard :album="album"/>
            </div>
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
import SelectBar from '../../components/commons/SelectBar'
import axios from 'axios'

export default {
    name: 'AlbumSection',
    components:{
        AlbumCard,
        SpinnerLoading,
        SelectBar,
    },
    data(){
        return{
            albums: [],
            searchedGenre: '',
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
    methods:{
        selectedGenr(genere){
            this.searchedGenre = genere;
        }
    },
    computed:{
        searchFilter(){
            return this.albums.filter((obj)=> obj.genre.includes(this.searchedGenre))
        }
    }

}
</script>

<style lang="scss" scoped>
</style>