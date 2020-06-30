<template>
  <div class="header__section" :class="{open: open}">
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
    <div class="container" :class="{open: open}">
      <div class="container__wrapper">
        <div class="menu__items">
          <nuxt-link 
            class="menu__link" 
            to="/" 
          >
            <span data-content="Minor VD&FD" aria-hidden="true"></span>Minor VD&FD
            <Icons class-name="link__icon" type="arrow-right" />
          </nuxt-link>
          <nuxt-link 
            class="menu__link" 
            to="/sanne"
            @mouseover.native="hover = 'sanne'; kb = false"
            @mouseleave.native="hover = null; kb = true"
            ref="el"
          >
            <span data-content="Sanne van Zeijl" aria-hidden="true"></span>Sanne van Zeijl
            <Icons class-name="link__icon" type="arrow-right" />
          </nuxt-link>
          <nuxt-link 
            class="menu__link" 
            to="/steven" 
            @mouseover.native="hover = 'steven'; kb = false"
            @mouseleave.native="hover = null; kb = true"
          >
            <span data-content="Steven Wu" aria-hidden="true"></span>Steven Wu
            <Icons class-name="link__icon" type="arrow-right" />
          </nuxt-link>
          <nuxt-link 
            class="menu__link"
            to="/djenna"
            @mouseover.native="hover = 'djenna'; kb = false"
            @mouseleave.native="hover = null; kb = true"
          >
            <span data-content="Djenna Bakker" aria-hidden="true"></span>Djenna Bakker
            <Icons class-name="link__icon" type="arrow-right" />
          </nuxt-link>
          <nuxt-link 
            class="menu__link" 
            to="/geert"
            @mouseover.native="hover = 'geert'; kb = false"
            @mouseleave.native="hover = null; kb = true"
          >
            <span data-content="Geert Heemskerk" aria-hidden="true"></span>Geert Heemskerk
            <Icons class-name="link__icon" type="arrow-right" />
          </nuxt-link>
          <button class="test" @click="test">test</button>
        </div>
      </div>
      <div class="image__holder">
        <figure>
          <img :class="{ active: hover == 'sanne' }" id="sanne" src="~/assets/images/imgTest.png" alt="imgTest" />
        </figure>
        <figure>
          <img :class="{ active: hover == 'steven'}" id="steven" src="~/assets/images/placeholder.png" alt="imgTest" />
        </figure>
        <figure>
          <img :class="{ active: hover == null }" id="kb" src="~/assets/images/intro-image.png" alt="imgTest" />
        </figure>
        <figure>
          <img :class="{ active: hover == 'djenna' }" id="djenna" src="~/assets/images/imgTest.png" alt="imgTest" />
        </figure>
        <figure>
          <img :class="{ active: hover == 'geert' }" id="geert" src="~/assets/images/placeholder.png" alt="imgTest" />
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
      hover: 'sanne',
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
  },
  methods: {
    test() {
      console.log(this.$refs.el);
    }
  }
}
</script>
<style lang="scss" scoped>

.test {
  position: absolute;
  z-index: 100;
  color: red;
}
.nuxt-link-exact-active {
  color: white;

  & .link__icon {
    transform: rotate(-180deg);
  }
}

.header {
  position: relative;
  height: 85px;
  width: 100%;
  top: 0;
  z-index: 10;

  &__section {
    position: fixed;
    width: 100%;
    top: 0; 
    left: 0;
    height: 85px;
    overflow: hidden;

    &.open {
      height: 100vh;
      z-index: 10;
    }
  }

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
    background-color: $c-background;

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
    padding-right: .2rem;
  }

  &__icon {
    width: 14px;
    height: 14px;
  }
}

.link {
  &__icon {
    margin-left: .3rem;
    width: 1.5rem;
    height: 1.5rem;
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
  height: calc(100% - 85px); // 100 - Height of header
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: $c-background;
  z-index: 9;
  opacity: 0;

  &.open {
    opacity: 1;
  }
}

a {
  color: rgba($c-text, .5);
  text-decoration: none;
  display: flex;
  margin: 2.5rem 0rem;
  font-family: $f-heading;
  font-size: 1.6rem;
  align-items: center;
}

.image__holder {
  visibility: hidden;
  display: none;
}

@media only screen and (min-width: $mq-tablet) {
  a {
    font-size: 3rem; 
    margin: 3.5rem 0;
  }

  .link__icon {
    width: 2rem;
    height: 2rem;
    margin-left: 1rem;
  }
}

@media only screen and (min-width: $mq-s-laptop) {
  figure {
    position: absolute;
  }

  a {
    font-size: 4rem;
    margin: 4.5rem 0;
  }

  .container {
    justify-content: center;
    text-align: left;

    &__wrapper {
      // position: absolute;
      margin: 0rem 4.5rem;
      left: 0;
      z-index: 1;
    }
  }

  // .image__holder {
  //   position: absolute;
  //   visibility: visible;
  //   display: block;
  //   width: 880px;
  //   height: 540px;
  //   margin: 0rem 0rem 0rem 2rem;
  // }

  .menu {
    &__button {
      display: none;
    }
  }

  .link__icon {
    width: 3rem;
    height: 3rem;
  }
}

@media only screen and (min-width: $mq-l-laptop) {
  figure {
    width: 80%;
    max-width: 1040px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    object-position: center;
    opacity: 0;
    transform: scale(0.6) translateX(15%);
    transition: all 0.8s cubic-bezier(0.23, 1, 0.32, 1);

    &.active { 
      display: initial;
      z-index: 1;
      opacity: 1;
      transition-delay: .2s;
      transform: scale(1) translateX(0);
    }
  }

  .menu {
    &__link {
      position: relative;
      transition: transform 0.8s cubic-bezier(0.23, 1, 0.32, 1);

      &:hover {
        transform: translateY(8%) translateX(-3%);

        span {
          transform: translateY(0);
          
          &:before {
            transform: translateY(0);
          }
        }
      }

      span {
        position: absolute;
        left: 0;
        overflow: hidden;
        transform: translateY(100%);
        transition: transform 0.8s cubic-bezier(0.23, 1, 0.32, 1);

        &:before {
          display: inline-block;
          content: attr(data-content);
          color: white;
          transform: translateY(-100%);
          transition: transform .8s cubic-bezier(.23, 1, .32, 1);
        }
      }
    }
  }

  a {
    font-size: 2.5rem;
    margin: 4rem 0;
  }

  .container {
    &__wrapper {
      margin: 0rem 5.5rem;
    }
  }

  .image__holder {
    width: 1040px;
    height: 580px;
    position: absolute;
    visibility: visible;
    display: block;
  }

  .link__icon {
    display: none;
  }
}

@media only screen and (min-width: $mq-xl-laptop) {
  .menu {
    &__link {
      font-size: 4rem;
      margin: 5rem 0;
    }
  }
}

@media only screen and (min-width: $mq-desktop) {
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
