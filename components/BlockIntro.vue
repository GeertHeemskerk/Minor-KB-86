<template>
  <div class="section__wrapper">
    <h2 class="block__title" :class="author">{{ title }}</h2>
    <div class="block__divider"></div>
    <p class="block__text">{{ text }}</p>
    <a class="block__link block__link--button" :class="author" v-if="link" :href="link" target="_blank" rel="noopener">
      <span v-if="linkText">
        {{ linkText }}
      </span>
    </a>
  </div>
</template>
<script>
export default {
  props: {
    author: String,
    title: String,
    text: String,
    link: String,
    linkText: String
  }
}
</script>
<style lang="scss" scoped>

h2.sanne {
  color: $c-sanne;
}

h2.steven {
  color: $c-steven-darker;
}

h2.geert {
  color: $c-geert;
}

h2.djenna {
 color: $c-djenna;
}

a.sanne:hover {
  cursor: url("~assets/cursors/hand-sanne.png"), auto;
}

a.steven {
  color: black;
  &:hover {
    cursor: url("~assets/cursors/hand-home.png"), auto;
  }
}

a.geert:hover {
  cursor: url("~assets/cursors/hand-geert.png"), auto;
}

a.djenna:hover {
  cursor: url("~assets/cursors/hand-djenna.png"), auto;
}

.section {
  &__wrapper {
    padding: 5rem 2.8rem 2rem 2.8rem;
    text-align: center;
  }
}

.block {
  &__title {
    font-size: 1.875rem;
    text-align: center;
  }

  &__divider {
    margin: 1rem auto;
    width: 2px;
    height: 1.2rem;
    background-color: black;
  }

  &__text {
    text-align: center;
    font-size: .7rem;
    line-height: 1.3rem;
    padding-bottom: 2.5rem;
  }

  &__link {
    display: block;
    text-align: center;
    font-weight: bold;

    &--button {
      color: white;
      position: relative;
      padding: .8rem 2rem;
      text-align: center;
      display: inline-block;
      text-decoration: none;
      border: 2px solid black;
      font-family: $f-heading;
      font-weight: normal;
      letter-spacing: 1px;
      font-size: .8rem;

      &:hover {
        &:before {
          transform: translate(0, 0);
        }
      }

      &:before {
        content: '';
        position: absolute;
        width: 101%; //Some reason it has a gap
        height: 101%; //Some reason it has a gap
        transform: translate(7px, 7px);
        top: 0; 
        left: 0;
        z-index: -1;
        transition: transform .4s cubic-bezier(.23, 1, .32, 1);
      }

      &.sanne {
        &:before {
          background-color: $c-sanne;
        }
      }

      &.steven {
        &:before {
          background-color: $c-steven;
        }
      }

      &.djenna {
        &:before {
          background-color: $c-djenna;
        }
      }

      &.geert {
        &:before {
          background-color: $c-geert;
        }
      }
    }
  }
}

@media(min-width: $mq-tablet) {
  .section {
    &__wrapper {
      padding-left: 4rem;
      padding-right: 4rem;
      margin: 0 auto;
    }
  }

  .block {
    &__text {
      font-size: 1rem;
      line-height: 1.85rem;
    }

    &__link {
      font-size: 1rem;
    }
  }
}

@media(min-width: $mq-s-laptop) {
  .section {
    &__wrapper {
      max-width: 820px;
    }
  }

  .block {
    &__title {
      font-size: 2.5rem;
    }

    &__divider {
      height: 2.2rem;
    }
  }
}

@media(min-width: $mq-l-laptop) {}
@media(min-width: $mq-xl-laptop) {}
@media(min-width: $mq-desktop) {}
</style>