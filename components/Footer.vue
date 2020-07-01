<template>
  <div>
    <div :class="author" class="section__wrapper">
      <h2 :class="author">KB-86</h2>
      <nuxt-link :class="author" to="/sanne">Sanne</nuxt-link>
      <nuxt-link  :class="author" to="/steven">Steven</nuxt-link>
      <nuxt-link :class="author" to="/djenna">Djenna</nuxt-link>
      <nuxt-link :class="author" to="/geert">Geert</nuxt-link>
      <div class="link__projects">
        <h3>Bekijk ook projecten van onze medestudenten:</h3>
        <a :class="author" href="#">Groep 1</a>
        <a :class="author" href="#">Groep 3</a>
        <a :class="author" href="#">Groep 4</a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    author: String,
  }
}
</script>
<style lang="scss" scoped>
  .section__wrapper {
    text-align: center;
    width: 100%;
    padding: 2rem;

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

  a, h2, h3 {
    color: white;
    text-decoration: none;
  }

  h2 {
    font-size: 3rem;
    margin: 0 0 2rem 0;
  }

  a {
    margin: 0 0.2rem;

    &:hover {
      text-decoration: underline;
    }
  }

  h1.steven, a.steven {
    color: black;
  }

  h3 {
    font-size: 1.3rem;
    padding-bottom: 2rem;
  }

  a.sanne:hover {
    cursor: url("~assets/cursors/hand-sanne.png"), auto;
  }

  a.steven:hover {
    cursor: url("~assets/cursors/hand-steven.png"), auto;
  }

  a.geert:hover {
    cursor: url("~assets/cursors/hand-geert.png"), auto;
  }

  a.djenna:hover {
    cursor: url("~assets/cursors/hand-djenna.png"), auto;
  }

  .link {
    &__projects {
      margin: 3rem 0;
    }
  }

  @media(min-width: $mq-tablet) {
    .section__wrapper {
      padding: 4rem;
    }

    h1 {
      font-size: 4rem;
      margin: 0 0 2rem 0;
    }

    h3 {
      font-size: 1.7rem;
    }

    a {
      margin: 0 2rem;
    }
  }
</style>
