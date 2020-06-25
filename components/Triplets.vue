<template>
  <div>
    <div class="section__wrapper">
      <img :src="left" :alt="leftAlt">
      <img :src="middle" :alt="middleAlt">
      <img :src="right" :alt="rightAlt">
    </div>
  </div>
</template>
<script>
export default {
  props: {
    left: String,
    leftAlt: String,
    middle: String,
    middleAlt: String,
    right: String,
    rightAlt: String,
  },
}
</script>
<style lang="scss" scoped>
  .section__wrapper {
    width: 100%;
    padding: 1.5rem 3rem;
  }

  img {
    display: block;
    width: 100%;
    height: auto;
    position: relative;
    margin-bottom: 3rem;
  }

  @media only screen and (min-width: $mq-tablet) {
    .section__wrapper {
      display: flex;
      padding: 3rem 0 8rem 0;
    }

    img {
      width: 30%;
      margin-bottom: 0;
    }

    img:nth-child(2) {
      margin: 0 5%;
      top: 3rem;
    }
  }

  @media only screen and (min-width: $mq-s-laptop) {
    img:nth-child(2) {
      top: 4rem;
    }
  }

  @media only screen and (min-width: $mq-xl-laptop) {
    img:nth-child(2) {
      top: 5rem;
    }
  }

  @media only screen and (min-width: $mq-desktop) {
    img:nth-child(2) {
      top: 6rem;
    }

    .section {
      &__wrapper {
        padding-bottom: 11rem;
      }
    }
}
</style>
