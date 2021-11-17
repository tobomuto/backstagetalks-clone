<template>
  <section>
    <div class="cover">
      <img :src="require(`../assets/covers/${issue.cover}.png`)"  alt="">
      <p>{{ issue.title }}</p>
      <a :href="issue.link">BUY HERE</a>
      <p v-if="issue.isAvailable == true">
        or in <a href="https://backstagetalks.com/stocklist.php">selected store</a>.
      </p>
      <p v-if="issue.isAvailable == false">
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
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid black;
  height: 812px;
  scroll-snap-align: start;
  .cover {
    display: flex;
    flex-direction: column;
    align-items: center;
    img {
      width: 80%;
      max-width: 420px;
      height: auto;
    }
    p {
      padding: 15px;
      text-align: center;
    }
  }

}

</style>