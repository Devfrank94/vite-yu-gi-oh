<script>

export default {
  name: "Header",
  data(){
    return{
      
    }
  }
}
</script>

<template>


  <div class="container-fluid d-flex al-item-cent">
    <img src="../assets/img/Logo Yu-Gi-Oh.png" alt="Logo">
  <h1>Yu-Gi-Oh Api</h1>

  </div>

</template>

<!-- Al'interno del tag style dobbiamo scrivere lang="scss" per poter utilizzare sass all'interno -->
<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.container-fluid{
  img{
    width: 100px;
    margin: 1.5rem .5rem;
  }

  h1{
  font-size: 2rem;
  font-weight: 600;
}

}

</style>