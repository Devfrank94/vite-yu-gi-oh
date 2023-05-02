<script>
export default {
  name:'Main',
  data(){
    return {
    
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

        <h3>Found 39 cards</h3>

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