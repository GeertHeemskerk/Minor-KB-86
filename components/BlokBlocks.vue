<template>
  <div>
    <div class="section__wrapper">
      <div class="blok__holder">
        <p>{{ introText }}</p>
      </div>
      <div v-lazy-container="{ selector: 'img' }" class="blok__holder" :class="author">
        <img 
          :data-src="blokImage" 
          :data-loading="blokImageLoading" 
          :src="blokImage" 
          :alt="altImage">
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    introText: String,
    author: String,
    blokImage: String,
    blokImageLoading: String,
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

    &.sanne {
      background-color: $c-sanne;
    }

    &.steven {
      background-color: $c-steven;
    }

    &.geert {
      background-color: $c-geert;
    }

    &.djenna {
      background-color: $c-djenna;
    }
  }

  img {
    width: 200px;
  }
  
  p {
    font-size: .7rem;
    line-height: 1.3rem;
  }

  @media(min-width: $mq-tablet) {
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

  @media(min-width: $mq-s-laptop) {
    .section__wrapper {
      display: flex;
      margin: 5rem 0rem;
    }

    .blok__holder {
      width: 50%;
    }
  }

  @media(min-width: $mq-xl-laptop) {
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

  @media(min-width: $mq-desktop) {
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
