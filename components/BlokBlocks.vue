<template>
  <div>
    <div class="section__wrapper">
      <div class="blok__holder">
        <p> {{ introText }}</p>
      </div>
      <div class="blok__holder" :class="author">
        <img :src="blokImage" :alt="altImage">
      </div>
    </div>
  </div>
</template>
<script>
import Icons from '~/components/Icons.vue';

export default {
  components: {

  },
  props: {
    introText: String,
    author: String,
    blokImage: String,
    altImage: String,
  }
}
</script>
<style lang="scss" scoped>
  .section__wrapper {
    text-align: center;
    margin: 0 auto;
    margin: 3rem 0rem;
  }

  .blok__holder {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 400px;
    padding: 0 2rem;
  }

  img {
    width: 200px;
  }

  .subcolor--steven {
    background-color: $c-steven;
  }

  .subcolor--sanne {
    background-color: $c-sanne;
  }

  .subcolor--geert {
    background-color: $c-geert;
  }

  .subcolor--djenna {
    background-color: $c-djenna-light;
  }

  p {
    font-size: .7rem;
    line-height: 1.3rem;
  }

  @media only screen and (min-width: $mq-tablet) {
    .section__wrapper {
      margin: 4rem 0rem;
    }

    .blok__holder {
      justify-content: center;
      align-items: center;
      flex-direction: row;
      padding: 0rem 4rem;
    }

    img {
      width: 250px;
    }

    p {
      font-size: 1rem;
      line-height: 1.85rem;
    }
  }

  @media only screen and (min-width: $mq-s-laptop) {
    .section__wrapper {
      display: flex;
      margin: 5rem 0rem;
    }

    .blok__holder {
      width: 50%;
    }
  }

  @media only screen and (min-width: $mq-xl-laptop) {
    .section__wrapper {
      margin: 7rem 0rem;
    }

    .blok__holder {
      padding: 0rem 7rem;
      height: 550px;
    }

    img {
      width: 300px;
    }
  }

  @media only screen and (min-width: $mq-desktop) {
    .section__wrapper {
      margin: 9rem 0rem;
    }

    .blok__holder {
      padding: 0rem 14rem;
      height: 750px;
    }

    img {
      width: 375px;
    }
  }

</style>
