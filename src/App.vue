<template>
  <div id="app">

    <Header/>

    <Home/>

  </div>
</template>

<script>

import Home from './pages/Home.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Home,
    Header
  },
  data() {
    return {
      section: 0,
      windowTop: 0
    }
  },
  computed: {
  }
}
</script>

<style lang="scss">

html {
  transition: all 700ms ease 0s;
  // overflow-y: scroll;
  // -ms-overflow-style: none;  /* IE and Edge */

  height: 100vh;
  // scroll-snap-type: mandatory;
  // scroll-snap-points-y: repeat(100vh);
  scroll-snap-type: y mandatory;
  // &::-webkit-scrollbar { /* Hide scrollbar for Chrome, Safari and Opera */
  //   display: none;
  // }
  scrollbar-width: none;  /* Firefox */
}

body {
  margin: 0;
}



</style>
