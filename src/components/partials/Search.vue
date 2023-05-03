
<script>

import { store } from '../../data/store'
export default {
  name: 'Search',
  data(){
    return{
      store
    }
  }
}
</script>

<template>

  <select class="m-3" name="" id="">
    <option value="" selected>Seleziona il filtro</option>
    <option v-for="(type) in store.typeMonsterArr" :key="type" value="type">{{ type }}</option>
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
