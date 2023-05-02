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
    <div class="info pt-3">
      <h5 class="py-1">{{ name }}</h5>
      <span class="py-3">{{ type }}</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.fm-card{
  text-align: center;
  

  .info{
    background-color: $bg-primary;
    height: 100px;

    h5{
      color: white;
      font-size: .8rem;
      font-weight: 700;
      text-transform: uppercase;
    }

  }

}


</style>