
<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import Footer from "./components/Footer.vue"

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
    Footer
  },

  methods:{
    getApi(){
      axios.get(store.apiUrl + "?num=105&offset=0") // aggiunto per evitare che axios richiami tutte le carte contemporaneamente
      .then(result => {
        store.cardArray = result.data.data;
        console.log(store.cardArray)
      })
    }
  },
  mounted(){
    this.getApi();
  }
}

</script>
<template>

  <Header />

  <Main />

  <Footer />

  
</template>


<style lang="scss">

  @use './scss/main.scss' as *;

</style>