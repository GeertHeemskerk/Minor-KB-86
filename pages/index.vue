<template>
  <main class="main">
    <Header />
    <section class="content">
      <div class="content__wrapper">
        <div class="title__group">
          <nuxt-link to="/sanne" class="title__single title__single--hide">Sanne van Zeijl</nuxt-link>
          <nuxt-link to="/steven" class="title__single title__single--hide">Steven Wu</nuxt-link>
          <nuxt-link to="/" class="title__single title__single--title">SSDG</nuxt-link>
          <nuxt-link to="/geert" class="title__single title__single--hide">Geert Heemskerk</nuxt-link>
          <nuxt-link to="/djenna" class="title__single title__single--hide">Djenna Bakker</nuxt-link>
        </div>
        <figure class="intro__figure">
          <img class="intro__media" src="~/assets/images/intro-image.png" alt="verf die samenkomt">
        </figure>
        <p class="intro__text">De foto van de verf die samenkomt is een goede metafoor voor deze website. Een website die het werk van 4 leerlingen samenvoegt. In 3 blokken van 5 weken mochten de leerlingen hun eigen leerdoelen samen stellen. Nieuwsgierig? Kijk snel verder.</p>
      </div>
    </section>
  </main>
</template>

<script>
import Header from '~/components/Header.vue';
export default {
  components: {
    Header,
  }
}
</script>

<style scoped lang="scss">
.main {
  background-color: $c-background;
  width: 100vw;
  height: 100vh;
  position: relative;
  display: flex;
  flex-direction: column;
}

.content {
  position: absolute;
  display: flex;
  justify-content: center;
  top: 50%;
  transform: translateY(-50%);

  p, h1, h2, h3, h4, h5, h6 {
    color: $c-text;
  }

  &__wrapper {
    position: relative;
  }
}

.title {
  &__group {
    position: absolute;
    top: -1.4rem;
    z-index: 1;
    left: 50%;
    transform: translateX(-50%);
  }

  &__single {
    font-family: $f-heading;
    font-size: 2rem;
    text-decoration: none;
    color: white;

    &--hide {
      display: none;
    }
  }
}

.intro {
  &__figure {
    width: 75%;
    margin: 0 auto;
  }

  &__media {
    width: 100%;
    height: 414px;
    object-fit: cover;
    object-position: center;
  }

  &__text {
    position: absolute;
    bottom: -5rem;
    width: 60%;
    text-align: center;
    z-index: 1;
    left: 50%;
    transform: translateX(-50%);
    letter-spacing: 1px;
    font-size: 0.625rem;
    line-height: 185%;
  }
}

@media(min-width: $mq-tablet) {
  .title {
    &__group {
      position: static;
      text-align: center;
      left: unset;
      transform: none;
    }
  }

  .intro {
    &__figure {
      margin: 2rem auto;
    }

    &__text {
      position: static;
      bottom: unset;
      transform: none;
      text-align: center;
      margin: 0 auto;
    }
  }
}

@media(min-width: $mq-s-laptop) {
  .content {
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%;

    &__wrapper {
      margin: 0 4.5rem;
    }
  }

  .title {
    &__group {
      text-align: left;
      position: absolute;
      left: 0;
      top: 50%;
      transform: translateY(-50%);
    }

    &__single {
      margin-bottom: 2rem;
      display: block;
      font-size: 3rem;
      color: rgba(white, .3);

      &--hide {
        display: block;
      }

      &--title {
        color: white;
      }

      &:last-child {
        margin-bottom: 0;
      }
    }
  }

  .intro {
    &__text {
      position: absolute;
      font-size: 1rem;
      text-align: right;
      bottom: -5rem;
      right: 0;
      left: unset;
      transform: none;
      width: 50%;
    }

    &__figure {
      width: 75%;
    }

    &__media {
      height: 500px;
    }
  }
}

@media(min-width: $mq-l-laptop) {
  .content {
    &__wrapper {
      width: 85%;
      max-width: 1300px;
    }
  }

  .title {
    &__single {
      margin-bottom: 3rem;
    }
  }

  .intro {
    &__text {
      bottom: -3rem;
    }
  }
}

@media(min-width: $mq-desktop) {
  .title {
    &__single {
      margin-bottom: 5rem;
    }
  }
}
</style>
