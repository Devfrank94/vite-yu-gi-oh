<script>
import {store} from "../data/store.js";
import Card from "./Card.vue";

export default {
  name:'Main',
  components:{
    Card
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
      <select class="m-3" name="" id="">
        <option value="Alien">Alien</option>
      </select>

      <div class="container-fluid p-4">

        <h3>Found {{store.cardArray.length}} cards</h3>

        <div class="row row-cols-5 m-0 test2">
          <div class="col test">
            <Card v-for ="card in store.cardArray" :key="card.id" :img="card.image_url" :name="card.name" :archetype="card.archetype" />
            
          </div>
        </div>

      </div>

    </div>





  </body>


  
</template>


<style lang="scss" scoped>
  @use '../scss/main.scss' as *;

  body{
    background-color: $bg-primary;
    height: 700px; // da rimuovere

    select{
    border-radius: 5px;
    padding: 5px;
    min-width: 150px;
    border: 0;
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
}


</style>