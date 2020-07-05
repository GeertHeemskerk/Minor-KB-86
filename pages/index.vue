<template>
  <main class="main">
    <Header class-name="header--home" />
    <section class="content">
      <div class="content__wrapper">
        <div class="title__group">
          <nuxt-link
            to="/"
            class="title__single title__single--title"
            title="Ga naar de start pagina"
          >
            <span data-content="Minor VD&FD" aria-hidden="true"></span>Minor VD&FD
          </nuxt-link>
          <nuxt-link
            to="/sanne"
            class="title__single title__single--hide"
            title="Ga naar het werk van Sanne van Zeijl"
            @mouseover.native="hover = 'sanne';"
            @mouseleave.native="hover = null;"
          >
            <span data-content="Sanne van Zeijl" aria-hidden="true"></span>Sanne van Zeijl
          </nuxt-link>
          <nuxt-link
            to="/steven"
            class="title__single title__single--hide"
            title="Ga naar het werk van Steven Wu"
            @mouseover.native="hover = 'steven';"
            @mouseleave.native="hover = null;"
          >
            <span data-content="Steven Wu" aria-hidden="true"></span>Steven Wu
          </nuxt-link>
          <nuxt-link
            to="/djenna"
            class="title__single title__single--hide"
            title="Ga naar het werk van Djenna Bakker"
            @mouseover.native="hover = 'djenna';"
            @mouseleave.native="hover = null;"
          >
            <span data-content="Djenna Bakker" aria-hidden="true"></span>Djenna Bakker
          </nuxt-link>
          <nuxt-link
            to="/geert"
            class="title__single title__single--hide"
            title="Ga naar het werk van Geert Heemskerk"
            @mouseover.native="hover = 'geert';"
            @mouseleave.native="hover = null;"
          >
            <span data-content="Geert Heemskerk" aria-hidden="true"></span>Geert Heemskerk
          </nuxt-link>
        </div>
        <figure v-lazy-container="{ selector: 'img' }" class="intro__figure">
          <img
            class="intro__media"
            :class="{ 'intro__media--hover': hover == 'sanne' }"
            :data-src="require('~/assets/images/profile-sanne.png')"
            :data-loading="require('~/assets/images/profile-sanne.png?lqip')"
            alt="Foto van Sanne"
          />
          <img
            class="intro__media"
            :class="{ 'intro__media--hover': hover == 'steven' }"
            :data-src="require('~/assets/images/profile-steven.png')"
            :data-loading="require('~/assets/images/profile-steven.png?lqip')"
            alt="Foto van Steven"
          />
          <video
            class="intro__media"
            :class="{ 'intro__media--hover': hover == null }"
            autoplay
            loop
            muted
            playsinline
          >
            <source src="~/assets/videos/homevideo.mp4" type="video/mp4">
          </video>
          <img
            class="intro__media"
            :class="{ 'intro__media--hover': hover == 'geert' }"
            :data-src="require('~/assets/images/profile-geert.png')"
            :data-loading="require('~/assets/images/profile-geert.png?lqip')"
            alt="Foto van Geert"
          />
          <img
            class="intro__media"
            :class="{ 'intro__media--hover': hover == 'djenna'}"
            :data-src="require('~/assets/images/profile-djenna.png')"
            :data-loading="require('~/assets/images/profile-djenna.png?lqip')"
            alt="Foto van Djenna"
          />
        </figure>
        <section class="intro__text">
          <p class="intro__text-content" :class="{ 'intro__text-content--hover': hover == 'sanne' }">Hier vind je het werk van Sanne, zij heeft zich dit blok vooral gefocust op het leren van 3D motion design. Voor de minor had ze nog helemaal geen ervaring maar heeft in de afgelopen 15 weken veel geleerd! Klik en zie haar werk.</p>
          <p class="intro__text-content" :class="{ 'intro__text-content--hover': hover == 'steven' }">Steven, een toekomstige front-end developer die zich verder willen ontwikkelen in het gebied van design en development. Zo heeft hij in afgelopen half jaar veel geleerd over ontwerpen en website bouwen. Klik verder om zijn werk te zien.</p>
          <p class="intro__text-content" :class="{ 'intro__text-content--hover': hover == null }">In de minor Visual Design & Front-end Development mochten studenten zelf bepalen wat zij in een half jaar wilde leren. De animatie is een goede metafoor voor het samenkomen van het werk van vier studenten op een plek. Vanuit dit concept hebben we de website opgebouwd. Nieuwsgierig? Klik dan op een van de individuele pagina’s van de vier studenten!</p>
          <p class="intro__text-content" :class="{ 'intro__text-content--hover': hover == 'geert' }">In de afgelopen maanden heeft Geert met Cinema 4D, Adobe pakket Photoshop, After Effects, XD en gewerkt, en met front-end technieken zoals SASS en NuxtJS(VueJS) gewerkt en is flink gegroeid binnen deze technieken. Klik en zie zijn werk.</p>
          <p class="intro__text-content" :class="{ 'intro__text-content--hover': hover == 'djenna' }">Djenna heeft zich de afgelopen maanden gefocust op het maken van logo’s en van web animaties. Van web animaties wist Djenna nog helemaal niets, en in de afgelopen weken in haar kennis hiervan flink gegroeid! Klik en zie haar werk.</p>
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
      hover: null,
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
    // position: absolute;
    // top: -1.4rem;
    // z-index: 2;
    // left: 50%;
    // transform: translateX(-50%);
    text-align: center;
    margin-bottom: 1rem;
  }

  &__single {
    position: relative;
    font-family: $f-heading;
    font-size: 2rem;
    text-decoration: none;
    color: white;
    transition: all .8s cubic-bezier(.23, 1, .32, 1);

    &--hide {
      display: none;
    }

    span {
      position: absolute;
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
      cursor: url("~assets/cursors/hand-home.png"), auto;
      transform: translate(-4%, 8%);

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
    height: 390px;
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

    &-content {
      display: none;

      &--hover {
        display: block;
      }
    }
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

    &__media {
      height: 414px;
    }

    &__text {
      position: static;
      bottom: unset;
      transform: none;
      text-align: center;
      margin: 0 auto;
      font-size: 1rem;
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
      z-index: 2;
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

      &-content {
        display: initial;
        position: absolute;
        right: 0;
        bottom: 0;
        opacity: 0;
        transform: translate(8%, 8%) skewY(4deg);
        transition: all .8s cubic-bezier(.23, 1, .32, 1);

        &--hover {
          display: initial;
          opacity: 1;
          transform: translate(0%) skewY(0deg);
          transition-delay: .3s;
        }
      }
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
        transition-delay: .2s;
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
  .title {
    &__single {
      font-size: 4rem;
    }
  }

  .intro {
    &__figure {
      height: 620px;
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
