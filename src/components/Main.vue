<script>
import {store} from "../data/store.js";
import Card from "./Card.vue";
import Search from "./partials/Search.vue";

export default {
  name:'Main',
  components:{
    Card,
    Search
  },
  data(){
    return {
    store
    }
  },
}

</script>
<template>
  <body>
    
    <div class="fmcontainer">
      
      <search/>

      <div class="container-fluid p-4">

        <h3>Found {{store.cardArray.length}} cards</h3>

        <div class="row row-cols-5">
            <Card
              v-for
              ="card in store.cardArray"
              :key="card.id"
              :img="card.card_images"
              :name="card.name"
              :type="card.archetype || card.type" />
              <!-- Nel caso in cui non c'è l'archetipo viene sostituito dal tipo -->
            
        </div>

      </div>

    </div>





  </body>


  
</template>


<style lang="scss" scoped>
  @use '../scss/main.scss' as *;

  body{
    background-color: $bg-primary;

  }

  .fmcontainer{

    .container-fluid{
      background-color: white;

    h3{
    background-color: $bg-secondary;
    color: white;
    font-size: .8rem;
    font-weight: 700;
    padding: 1rem;
    }

    }

  }


</style>