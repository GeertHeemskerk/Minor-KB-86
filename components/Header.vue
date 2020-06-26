<template>
  <div>
    <header class="header" :class="[className, { 'header--open': open }]">
      <div class="header__wrapper">
          <transition name="slide-fade">
            <button class="menu__button button--clean" v-if="!open" key="on" @click="open = true">
              <div class="menu">
                <p class="menu__text">Menu</p>
                <Icons class-name="menu__icon" type="menu" />
              </div>
            </button>
            <button class="menu__button button--clean" v-else key="off" @click="open = false">
              <div class="menu">
                <p class="menu__text">Close Menu</p>
                <Icons class-name="menu__icon" type="menu-close" />
              </div>
            </button>
          </transition>
        </div>
    </header>
    <div v-if="open" class="container">
      <div class="container__wrapper">
        <div class="menu__items">
          <nuxt-link to="/" data-text="KB-86 SSDG >>">
            KB-86 SSDG >>
          </nuxt-link>
          <nuxt-link to="/djenna" data-text="Djenna Bakker >>" @mouseover.native="djenna = true; kb = false"  @mouseleave.native="djenna = false; kb = true">
            Djenna Bakker >>
          </nuxt-link>
          <nuxt-link to="/geert" data-text="Geert Heemskerk >>" @mouseover.native="geert = true; kb = false"  @mouseleave.native="geert = false; kb = true">
            Geert Heemskerk >>
          </nuxt-link>

          <nuxt-link to="/sanne" data-text="Sanne van Zeijl >>" @mouseover.native="sanne = true; kb = false"  @mouseleave.native="sanne = false; kb = true" >
            Sanne van Zeijl >>
          </nuxt-link>
          <nuxt-link to="/steven" data-text="Steven Wu >>" @mouseover.native="steven = true; kb = false"  @mouseleave.native="steven = false; kb = true">
            Steven Wu  >>
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
        <figure>
          <img v-bind:class="{ active: kb }" id="kb" src="~/assets/images/intro-image.png" alt="imgTest">
        </figure>
        <figure>
          <img v-bind:class="{ active: djenna }" id="djenna" src="~/assets/images/imgTest.png" alt="imgTest">
        </figure>
        <figure>
          <img v-bind:class="{ active: geert }" id="geert" src="~/assets/images/placeholder.png" alt="imgTest">
        </figure>
      </div>
    </div>
  </div>
</template>
<script>
import Icons from '~/components/Icons.vue';

export default {
  data() {
    return {
      open: false,
      sanne: false,
      steven: false,
      kb: true,
      djenna: false,
      geert: false,
    }
  },
  components: {
    Icons,
  },
  props: {
    className: String
  }
}
</script>
<style lang="scss" scoped>
.header {
  height: 85px;
  width: 100%;
  position: absolute;
  top: 0;
  z-index: 10;

  &__wrapper {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    width: 90%;
    margin: 0 auto;
    height: 100%;
  }

  &--home {
    .menu {
      color: white;

      &__icon {
        stroke: white;
      }
    }
  }

  &--personal {
    position: sticky;

    .menu {
      color: black;

      &__button {
        display: block;
      }

      &__icon {
        stroke: black;
      }
    }
  }

  &--open {
    position: absolute;

    .menu {
      color: white;

      &__icon {
        stroke: white;
      }
    }
  }
}

.menu {
  display: flex;
  align-items: center;

  &__button {
    cursor: pointer;
  }

  &__text {
    font-family: $f-heading;
    font-size: 0.625rem;
    letter-spacing: 1px;
    padding-right: 1rem;
  }

  &__icon {
    width: 14px;
    height: 14px;
  }
}

.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all .6s;
}

.slide-fade-enter,
.slide-fade-leave-active {
  opacity: 0;
}

.slide-fade-enter {
  transform: translateX(31px);
}

.slide-fade-leave-active {
  transform: translateX(-31px);
}

.container {
  position: relative;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: $c-background;
  z-index: 9;
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

  .menu {
    &__button {
      display: none;
    }
  }
}

@media only screen and (min-width: $mq-l-laptop) {
  a {
    font-size: 2.4rem;
    margin: 4rem 0;
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
