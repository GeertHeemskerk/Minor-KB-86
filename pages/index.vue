<template>
  <main class="main">
    <Header class-name="header--home" />
    <section class="content">
      <div class="content__wrapper">
        <div class="title__group">
          <nuxt-link 
            to="/sanne"
            class="title__single title__single--hide"
            @mouseover.native="sanne = true; kb = false"
            @mouseleave.native="sanne = false; kb = true"
          >
            <span data-content="Sanne van Zeijl" aria-hidden="true"></span>Sanne van Zeijl
          </nuxt-link>
          <nuxt-link 
            to="/steven"
            class="title__single title__single--hide"
            @mouseover.native="steven = true; kb = false"
            @mouseleave.native="steven = false; kb = true"
          >
            <span data-content="Steven Wu" aria-hidden="true"></span>Steven Wu
          </nuxt-link>
          <nuxt-link 
            to="/"
            class="title__single title__single--title"
          >
            <span data-content="SSDG" aria-hidden="true"></span>SSDG
          </nuxt-link>
          <nuxt-link 
            to="/geert"
            class="title__single title__single--hide"
            @mouseover.native="geert = true; kb = false"
            @mouseleave.native="geert = false; kb = true"
          >
            <span data-content="Geert Heemskerk" aria-hidden="true"></span>Geert Heemskerk
          </nuxt-link>
          <nuxt-link 
            to="/djenna"
            class="title__single title__single--hide"
            @mouseover.native="djenna = true; kb = false"
            @mouseleave.native="djenna = false; kb = true"
          >
            <span data-content="Djenna Bakker" aria-hidden="true"></span>Djenna Bakker
          </nuxt-link>
        </div>
        <figure class="intro__figure">
          <img class="intro__media" :class="{ 'intro__media--hover': sanne }" src="~/assets/images/placeholder.png" alt="Foto van Sanne">
          <img class="intro__media" :class="{ 'intro__media--hover': steven }" src="~/assets/images/placeholder-landscape.jpg" alt="Foto van Steven">
          <img class="intro__media" :class="{ 'intro__media--hover': kb }" src="~/assets/images/intro-image.png" alt="verf die samenkomt">
          <img class="intro__media" :class="{ 'intro__media--hover': geert }" src="~/assets/images/placeholder-portrait.jpg" alt="Foto van Geert">
          <img class="intro__media" :class="{ 'intro__media--hover': djenna }" src="~/assets/images/placeholder-portrait-girl.jpg" alt="Foto van Djenna">
        </figure>
        <section class="intro__text">
          <p class="intro__content">De foto van de verf die samenkomt is een goede metafoor voor deze website. Een website die het werk van 4 leerlingen samenvoegt. In 3 blokken van 5 weken mochten de leerlingen hun eigen leerdoelen samen stellen. Nieuwsgierig? Kijk snel verder.</p>
        </section>
      </div>
    </section>
  </main>
</template>

<script>
import Header from '~/components/Header.vue';
export default {
  data() {
    return {
      sanne: false,
      steven: false,
      kb: true,
      djenna: false,
      geert: false,
    }
  },
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
  width: 100%;

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
    z-index: 2;
    left: 50%;
    transform: translateX(-50%);
  }

  &__single {
    position: relative;
    font-family: $f-heading;
    font-size: 2rem;
    text-decoration: none;
    color: white;
    transition: transform .8s cubic-bezier(.23, 1, .32, 1);
    
    &--hide {
      display: none;
    }

    span {
      position: absolute;
      top: 0;
      left: 0;
      overflow: hidden;
      transform: translateY(100%);
      transition: transform .8s cubic-bezier(.23, 1, .32, 1);
      
      &::before {
        display: inline-block;
        content: attr(data-content);
        color: white;
        transform: translateY(-100%);
        transition: transform .8s cubic-bezier(.23, 1, .32, 1);
      }
    }

    &:hover {
      transform: translateY(8%) translateX(-3%);

      span {
        transform: translateY(0);
        &::before {
          transform: translateY(0);
        }
      }
    }
  }
}

.intro {
  &__figure {
    width: 75%;
    margin: 0 auto;
    position: relative;
  }

  &__media {
    width: 100%;
    height: 414px;
    object-fit: cover;
    object-position: center;
    display: none;

    &--hover {
      display: block;
    }
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
      width: 80%;
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
      display: inline-block;
      font-size: 3rem;
      color: rgba(white, .3);
      overflow: hidden;

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
      width: 60vw;
      max-width: 820px;
      height: 530px;
    }

    &__media {
      display: initial;
      position: absolute;
      height: 100%;
      object-fit: contain;
      object-position: center;
      transition: all .8s cubic-bezier(.23, 1, .32, 1);
      opacity: 0;
      transform: scale(0.7) translateX(-15%);

      &--hover {
        display: initial;
        z-index: 1;
        opacity: 1;
        transform: scale(1.0) translateX(0);
      }
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
      bottom: -1rem;
    }
  }
}

@media(min-width: $mq-xl-laptop) {
  .intro {
    &__figure {
      height: 550px;
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
