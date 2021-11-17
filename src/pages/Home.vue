<template>
  <div>
    <section class="issue#5"></section>
    <p>{{ windowTop }}</p>
    <section v-for="issue in issues" :key="issue.title"></section>

</div>
</template>

<script>

import issuesJson from '../data/issues.json';

export default {
  components: {
  },
  data() {
    return {
      issues: issuesJson,
      section: 0,
      windowTop: 0
    }
  },
  mounted() {
    let self = this;
    window.addEventListener("scroll", function() {
      self.windowTop = window.scrollY;
      self.windowSize = window.innerHeight;
    });
  },
}
</script>

<style lang="scss">

section {
  border: 1px solid black;
  height: 812px;
  scroll-snap-align: start;
}

</style>