<template>
  <div>
    <section class="issue#5"></section>
    <p>{{ windowTop }}</p>
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

</style>