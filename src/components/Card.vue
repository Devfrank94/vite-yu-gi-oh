<script>
export default {
  name: 'Card',
  props:{
    img:Array,
    name:String,
    type:String,
  }
}
</script>

<template>
  <div class="fm-card col mb-3">
    <img :src="img[0].image_url" :alt="name">
    <h5>{{ name }}</h5>
    <span>{{ type }}</span>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.fm-card{
  text-align: center;
}


</style>