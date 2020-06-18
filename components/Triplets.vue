<template>
  <div>
    <div class="section__wrapper">
      <img :src="left" :alt="altImage1">
      <img :src="middle" :alt="altImage2">
      <img :src="right" :alt="altImage3">
    </div>
  </div>
</template>
<script>
import Icons from '~/components/Icons.vue';

export default {
  components: {

  },
  props: {
    left: String,
    middle: String,
    right: String
  }
}
</script>
<style lang="scss" scoped>
  .section__wrapper {
    width: 100%;
    padding: 1.5rem 3rem;
  }

  img {
    width: 100%;
    height: 375px;
    margin: 1.5rem 0rem;
  }

  @media only screen and (min-width: $mq-tablet) {
    .section__wrapper {
      display: flex;
      padding: 1.5rem 0rem;
    }

    img {
      width: 30%;
      height: 315px;
    }

    img:nth-child(2) {
      margin: 0 5%;
      margin-top: 3rem;
    }
  }

  @media only screen and (min-width: $mq-s-laptop) {
    img {
      height: 375px;
    }

    img:nth-child(2) {
      margin-top: 4rem;
    }
  }

  @media only screen and (min-width: $mq-xl-laptop) {
    img {
      height: 500px;
    }

    img:nth-child(2) {
      margin-top: 5rem;
    }
  }

  @media only screen and (min-width: $mq-desktop) {
    img {
      height: 625px;
    }

    img:nth-child(2) {
      margin-top: 6rem;
    }
  }
</style>
