<template>
  <div>
    <div class="section__wrapper">
      <h1>{{ title }}</h1>
      <p> {{ text }}</p>
      <p :class="author" class="subject"> {{ subject }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: String,
    text: String,
    subject: String,
    author: String,
  }
}
</script>
<style lang="scss" scoped>
  .section__wrapper {
    text-align: center;
    padding: 0.2rem 2rem 1rem 2rem;
    max-width: 815px;
    margin: 0 auto;
  }

  h1 {
    font-size: 4rem;
    margin: 0 0 2rem 0;
  }

  p {
    font-size: 0.7rem;
    line-height: 1.3rem;
    margin: 0 0 2rem 0;
  }

  .subject {
    font-weight: bold;

    &.sanne {
      color: $c-sanne;
    }

    &.steven {
      color: $c-steven;
    }

    &.geert {
      color: $c-geert;
    }

    &.djenna {
      color: $c-djenna;
    }
  }
  
  @media only screen and (min-width: $mq-tablet) {
    .section__wrapper {
      padding: 0.3rem 4rem 1.4rem 4rem;
    }

    p {
      font-size: 1rem;
      line-height: 1.85rem;
      margin: 0 0 2rem 0;
    }
  }
</style>
