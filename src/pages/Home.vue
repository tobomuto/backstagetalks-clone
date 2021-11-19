<template>
  <div>
    <IssueSection v-for="issue in issues" :key="issue.title" :issue="issue"/>

</div>
</template>

<script>

import IssueSection from '../components/IssueSection';
import issuesJson from '../data/issues.json';

export default {
  components: {
    IssueSection
  },
  data() {
    return {
      issues: issuesJson,
      section: 0,
      windowTop: 0,
      windowSize: 0
    }
  },
  mounted() {
    let self = this;
    const htmlTag = document.querySelector('html');
    const sectionsTags = document.getElementsByTagName('section')
    let sectionTop0 = sectionsTags[0].offsetTop - 300;
    let sectionTop1 = sectionsTags[1].offsetTop - 300;
    let sectionTop2 = sectionsTags[2].offsetTop - 300;
    let sectionTop3 = sectionsTags[3].offsetTop - 300;
    let sectionTop4 = sectionsTags[4].offsetTop - 300;

    window.addEventListener("scroll", function() {
      self.windowTop = window.scrollY;
      self.windowSize = window.innerHeight;

      if (self.windowTop >= sectionTop0 && self.windowTop < sectionTop1) {
        htmlTag.style.backgroundColor = "#00c1b5"
      } else if (self.windowTop >= sectionTop1 && self.windowTop < sectionTop2) {
        htmlTag.style.backgroundColor = "#ff651a";
      } else if (self.windowTop >= sectionTop2 && self.windowTop < sectionTop3) {
        htmlTag.style.backgroundColor = "#ffbe00";
      } else if (self.windowTop >= sectionTop3 && self.windowTop < sectionTop4) {
        htmlTag.style.backgroundColor = "#1d3fbb";
      } else if (self.windowTop >= sectionTop4) {
        htmlTag.style.backgroundColor = "#e30512";
      }
    });
  },
}
</script>

<style lang="scss">

</style>