<template>
  <div id="footer">
    <p class="description">
      Backstage Talks is a&nbsp;magazine of&nbsp;casual, but in&nbsp;depth dialogues on&nbsp;design and business. Our decisions shape and influence this complex world—to have a&nbsp;chance to&nbsp;make the right ones, we need to talk.
      <br>
      <span class="copyright">© 2021 <a href="http://milk.sk/" target="_blank">Published by studio Milk</a></span>
      <br><br>
      <a href="/privacy-policy.php">Privacy Policy</a>
    </p>
    <p class="contact"><a href="mailto:info@backstagetalks.com">info@backstagetalks.com</a></p>
    <ul class="menu">
      <li v-for="issue in issues" :key="issue.id"><a :href="'#' + issue.id">{{ issue.title }}</a></li>
    </ul>
  </div>
</template>

<script>

import issuesJson from '../data/issues.json';

export default {
  data() {
    return {
      issues: issuesJson
    }
  }
}
</script>

<style lang="scss" scoped>

#footer {
  p {
    margin-top: 30px;
    margin-bottom: 50px;
    padding: 0 15px;
    font-size: 18px;
    font-weight: 700;
    text-align: center;
    line-height: 25px;
  }
  a {
    font-weight: 700;
    color: black;
  }
  .copyright {
    font-size: 12px;
    font-weight: normal;
    a {
      font-weight: normal;
    }
  }
  .contact {
    a {
      text-decoration: none;
    }
  }
  .menu {
    list-style: none;
    display: none;
    line-height: 1.6;
    a {
      font-weight: normal;
      text-decoration: none;
    }
  }
}

@media screen and (min-width:991px) {
  #footer {
    position: fixed;
    bottom: 0;
    width: 100vw;
    height: 100vh;
  }
  .menu {
    display: block !important;
    position: absolute;
    right: 50px;
    right: 15px;
    bottom: 0;
    text-align: right;
  }
  .description {
    text-align: left !important;
    position: absolute;
    bottom: 0;
    left: 22px;
    width: 320px;
    margin-bottom: 18px !important;
    padding: 0 !important;
  }
  .contact {
    text-align: right;
    position: absolute;
    margin-top: 0 !important;
    right: 0;
    top: 20px;
  }
}

</style>