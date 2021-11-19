<template>
  <div id="app">

    <Header/>

    <Home/>

    <Footer/>

  </div>
</template>

<script>

import Footer from './components/Footer.vue';
import Home from './pages/Home.vue'
import Header from './components/Header.vue'


export default {
  name: 'App',
  components: {
    Home,
    Header,
    Footer
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

@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

html {
  font-family: 'Roboto', sans-serif;
  transition: all 700ms ease 0s;
  font-size: 18px;
  height: 100vh;
  // scroll-snap-type: mandatory;
  // scroll-snap-points-y: repeat(100vh);
  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
  background-color: #00c1b5;
}

body {
  margin: 0;
}



@media screen and (min-width:991px) {
  #app {
    padding-bottom: 140px; /* Correcting Chrome shitty behaviour that don't include margin-bottom at the end of the page. */
  }
  html {
    &::-webkit-scrollbar { /* Hide scrollbar for Chrome, Safari and Opera */
      display: none;
    }
    scrollbar-width: none;  /* Firefox */
  }
}

</style>
