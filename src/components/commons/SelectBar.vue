<template>
  <select class="form-select mb-3" aria-label="Default select example" v-model="selectedGenr" @change="$emit('sel', selectedGenr)">
  <option disabled value="">Seleziona un genere</option>
  <option value="Rock">Rock</option>
  <option value="Pop">Pop</option>
  <option value="Jazz">Jazz</option>
  <option value="Metal">Metal</option>
</select>
</template>

<script>
export default {
    name: 'SelectBar',
    data(){
        return{
            selectedGenr: '',
        }
    }
}
</script>

<style lang="scss" scoped>
    select{
        text-align: center;
        max-width: 50%;
    }
</style>