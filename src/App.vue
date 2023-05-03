
<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import Footer from "./components/Footer.vue"
import Loader from "./components/partials/Loader.vue";
import axios from 'axios';
import {store} from './data/store';

export default {
  name:'App',
  data(){
    return{
      store
    }
  },
  components:{
    Header,
    Main,
    Footer,
    Loader
  },

  methods:{
    getApi(){
      store.isLoad = true;
      axios.get(store.apiUrl, {
        params:{
          num: store.cardNumber,
          offset: store.cardOffset,
          type: store.optionType
        }
      })
      .then(result => {
        store.isLoad = false;
        store.cardArray = result.data.data;
        console.log(store.cardArray)
      })
    },

    getCardTypes(){
        axios.get(store.apiUrl).then(result => {
          const cards = result.data.data;
          cards.forEach(card => {
              if (!store.typeMonsterArr.includes(card.type)) {
                store.typeMonsterArr.push(card.type)
              }
          });
          console.log(store.typeMonsterArr);
        })
      }

  },
  mounted(){
    this.getApi();
    this.getCardTypes()
  }
}

</script>
<template>

  <Header />

  <Loader v-if="store.isLoad"/>

  <!-- Main e Footer contenuti in un div per permettere la condizione v-else in modo da apparire una volta che il loader scompare a sua volta per condizione soddisfatta -->
  <div v-else>

  <Main @cardFilter="getApi" />

  <Footer />

  </div>
  
</template>


<style lang="scss">

  @use './scss/main.scss' as *;

</style>