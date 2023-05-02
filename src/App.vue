
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
      axios.get(store.apiUrl)
      .then(result => {
        console.log(result.data)
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