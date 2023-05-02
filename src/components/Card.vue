<script>
export default {
  name: 'Card',
  props:{
    img:String,
    name:String,
    archetype:String,
  }
}
</script>

<template>
  <div class="fm-card col mb-3">
    <img :src="img" :alt="name">
    <h5>{{ name }}</h5>
    <span>{{ archetype }}</span>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.fm-card{
  text-align: center;
}


</style>