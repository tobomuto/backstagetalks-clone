<template>
  <div id="header">
    <img src="../assets/logo.png" alt="logo">
  </div>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>

#header {
  padding-top: 20px;
  position: absolute;
  left: 15px;
  top: 0;
  z-index: 2;
  img {
    width: 160px;
  }
}

@media screen and (min-width:991px) {
  #header {
    position: fixed;
    img {
      width: 260px !important;
    }
  }

}


</style>