<template>
  <section :id="issue.id">
    <div class="cover">
      <img :src="require(`../assets/covers/${issue.cover}.png`)"  alt="">
      <p class="cover_title">{{ issue.title }} <span v-if="issue.isAvailable == false"> is sold out.</span></p>
      <p class="cover_link" v-if="issue.isAvailable == true">
        <a :href="issue.link">BUY HERE</a>
      </p>
      <p class="cover_link" v-if="issue.isAvailable == true">
        or in <a href="https://backstagetalks.com/stocklist.php">selected stores</a>.
      </p>
      <p class="cover_link" v-if="issue.isAvailable == false">
        If you are lucky, you may get the last pieces in <a href="http://backstagetalks.com/stocklist.php">selected stores</a>.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  props: ["issue"]
}
</script>

<style lang="scss" scoped>

section {
  height: 812px;
  padding-top: 15px;
  // scroll-snap-align: start;
  .cover {
    transform: translateY(-50%);
    top: 50%;
    margin-top: 48vh;
    text-align: center;
    img {
      width: 80%;
      max-width: 420px;
      height: auto;
    }
    p {
      margin-top: 0;
      font-weight: 700;
      padding: 0 15px;
      text-align: center;
    }
    .cover_link {
      font-size: 15px;
      padding-top: 3px;
      line-height: 22px;
    }
    a {
      font-weight: 700;
      text-decoration: none;
      color: white;
    }
  }
}

@media screen and (min-width:767px) {
  section {
    scroll-snap-align: start;
  }
}

</style>