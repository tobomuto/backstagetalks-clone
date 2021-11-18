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
  </div>
</template>

<script>
export default {

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
    text-decoration: none;
  }
}

</style>