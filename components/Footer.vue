<template>
  <div>
    <div :class="author" class="section__wrapper">
      <h2 :class="author">Minor - Visual Design & Front-end Development</h2>
      <nuxt-link :class="author" to="/sanne" title="Ga naar het werk van Sanne">Sanne</nuxt-link>
      <nuxt-link  :class="author" to="/steven" title="Ga naar het werk van Steven">Steven</nuxt-link>
      <nuxt-link :class="author" to="/djenna" title="Ga naar het werk van Djenna">Djenna</nuxt-link>
      <nuxt-link :class="author" to="/geert" title="Ga naar het werk van Geert">Geert</nuxt-link>
      <div class="link__projects">
        <h3 :class="author">Bekijk ook portfolio van onze medestudenten:</h3>
        <a class="footer__link--portfolio" :class="author" href="https://wendylange.github.io/minor.kb-86/" target="_blank" rel="noopener" title="Ga naar portfolio website van Dave, Ploy, Tim en Wendy">Dave, Ploy, Tim en Wendy</a>
        <a class="footer__link--portfolio" :class="author" href="https://portfolio-steel-five.vercel.app/" target="_blank" rel="noopener" title="Ga naar portfolio website van Bo, Matthew en Wendy">Bo, Matthew en Wenyi</a>
        <a class="footer__link--portfolio" :class="author" href="#" title="Ga naar portfolio website van Andrew, Calvin, Shantusha en Stijn">Andrew, Calvin, Shantusha en Stijn</a>
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
    font-size: 2.1rem;
    margin: 0 0 2rem 0;
  }

  a {
    font-size: .7rem;
    margin: 0 0.2rem;

    &:hover {
      text-decoration: underline;
    }
  }

  h2.steven, a.steven {
    color: black;
  }

  h3 {
    font-size: 1.3rem;
    padding-bottom: 2rem;

    &.steven {
      color: black;
    }
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

  .footer {
    &__link {
      &--portfolio {
        display: block;
        margin-bottom: 1rem;
      }
    }
  }

  .link {
    &__projects {
      margin: 3rem 0;
    }
  }

  @media(min-width: $mq-tablet) {
    a {
      font-size: 1rem;
    }

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
