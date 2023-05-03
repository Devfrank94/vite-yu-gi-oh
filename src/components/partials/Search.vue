
<script>

import { store } from '../../data/store'
export default {
  name: 'Search',
  data(){
    return{
      store
    }
  },

  methods:{
    saveType(value){
      store.optionType = value;
      this.$emit('filterCards')
      console.log(store.optionType)
    }
  }
}
</script>

<template>

  <select v-model="store.optionType" class="m-3" name="" id="">
    <option @click="saveType(null)" selected>All Type Cards</option>
    <option v-for="(type) in store.typeMonsterArr" :key="type" @click="saveType(type)" value="type">{{ type }}</option>
  </select>

</template>

<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

  select{
    border-radius: 5px;
    padding: 5px;
    min-width: 150px;
    border: 0;
  }
</style>
