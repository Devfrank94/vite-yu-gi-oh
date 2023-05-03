<script>
export default {
  name: "Loader"
}
</script>

<template>
  <div class="container d-flex justify-content-center my-3">
    <div class="loader"></div>
  </div>
</template>

<style lang="scss" scoped>
 

 .loader {
  width: 72px;
  height: 72px;
  margin: 30px;
  display: grid;
  animation: spinner-plncf9 4.8s infinite;
}

.loader::before,
.loader::after {
  content: "";
  grid-area: 1/1;
  border: 11.5px solid;
  border-radius: 50%;
  border-color: #474bff #474bff #0000 #0000;
  mix-blend-mode: darken;
  animation: spinner-plncf9 1.2s infinite linear;
}

.loader::after {
  border-color: #0000 #0000 #dbdcef #dbdcef;
  animation-direction: reverse;
}

@keyframes spinner-plncf9 {
  100% {
  transform: rotate(1turn);
  }
}



</style>