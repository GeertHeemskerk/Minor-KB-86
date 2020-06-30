<!-- Can be deleted, Use components/Header.vue instead -->
<template>
  <div class="container">
    <div class="container__wrapper">
      <div class="menu__items">
        <nuxt-link to="/sanne" data-text="Sanne van Zeijl" @mouseover.native="sanne = true; kb = false"  @mouseleave.native="sanne = false; kb = true" >
          Sanne van Zeijl
        </nuxt-link>
        <nuxt-link to="/steven" data-text="Steven Wu" @mouseover.native="steven = true; kb = false"  @mouseleave.native="steven = false; kb = true">
          Steven Wu
        </nuxt-link>
        <nuxt-link to="/" data-text="KB-86 SSDG">
          KB-86 SSDG
        </nuxt-link>
        <nuxt-link to="/djenna" data-text="Djenna Bakker" @mouseover.native="djenna = true; kb = false"  @mouseleave.native="djenna = false; kb = true">
          Djenna Bakker
        </nuxt-link>
        <nuxt-link to="/geert" data-text="Geert Heemskerk" @mouseover.native="geert = true; kb = false"  @mouseleave.native="geert = false; kb = true">
          Geert Heemskerk
        </nuxt-link>
      </div>
    </div>
    <div class="image__holder">
      <figure>
        <img  v-bind:class="{ active: sanne }" id="sanne" src="~/assets/images/imgTest.png" alt="imgTest">
      </figure>
      <figure>
        <img v-bind:class="{ active: steven }" id="steven" src="~/assets/images/placeholder.png" alt="imgTest">
      </figure>
      <video autoplay>
        <source src="~/assets/videos/homevideo.mp4">
      </video>
      <figure>
        <img v-bind:class="{ active: djenna }" id="djenna" src="~/assets/images/imgTest.png" alt="imgTest">
      </figure>
      <figure>
        <img v-bind:class="{ active: geert }" id="geert" src="~/assets/images/placeholder.png" alt="imgTest">
      </figure>
    </div>
  </div>
</template>
<script>
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
  methods: {

  }
}
</script>

<style scoped lang="scss">
.container {
  position: relative;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: $c-background;
}

a {
  color: rgba($c-text, 0.5);
  text-decoration: none;
  display: block;
  margin: 2.5rem 0rem;
  font-family: $f-heading;
  font-size: 1.6rem;
}

.image__holder {
  visibility: hidden;
  display: none;
}

@media only screen and (min-width: $mq-s-laptop) {
  figure {
    position: absolute;
  }

  img {
    transition: 1.3s;
    opacity: 0;
    transform: scale(0.8)
  }

  img.active{
    transition-delay: 0.55s;
    animation: zoomIn 1.3s;
    opacity: 1;
    transform: scale(1.0);
  }

  a {
    font-size: 2rem;
    height: 2rem;
  }

  a:before {
    content: attr(data-text);
    color: $c-text;
    position: absolute;
    height: 0;
    overflow: hidden;
    transition: 0.8s;
    word-break: keep-all;
  }

  a:hover:before {
    height: 2.5rem;
  }

  .container {
    justify-content: center;
    align-items: left;
    text-align: left;

    &__wrapper {
      position: absolute;
      margin: 0rem 4.5rem;
      left: 0;
      z-index: 1;
    }
  }

  .image__holder {
    position: absolute;
    visibility: visible;
    display: block;
    width: 880px;
    height: 540px;
    margin: 0rem 0rem 0rem 2rem;
  }
}

@media only screen and (min-width: $mq-l-laptop) {
  a {
    font-size: 2.4rem;
  }

  a:hover:before {
    height: 2.9rem;
  }

  .container {
    &__wrapper {
      margin: 0rem 5.5rem;
    }
  }

  .image__holder {
      width: 1040px;
      height: 580px;
    margin: 0rem 0rem 0rem 2rem;
  }
}

@media only screen and (min-width: $mq-desktop) {
  a {
    height: 4rem;
  }

  .container {
    &__wrapper {
      margin: 0rem 8.5rem;
    }
  }

  .image__holder {
    width: 1240px;
    height: 780px;
    margin: 0rem;
  }

  figure, img {
    width: 100%;
    height: 100%;
  }
}
</style>
