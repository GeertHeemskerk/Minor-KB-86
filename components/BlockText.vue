<template>
  <div class="section__wrapper">
    <p class="block__text">{{ text }}</p>
    <a class="block__link block__link--button" :class="author" v-if="link" :href="link" target="_blank" rel="noopener" :title="linkTitle">
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
    text: String,
    link: String,
    linkText: String,
    linkTitle: String,
  }
}
</script>
<style lang="scss" scoped>
a.sanne {
  color: $c-sanne;
  &:hover {
    cursor: url("~assets/cursors/hand-sanne.png"), auto;
  }
}

a.steven {
  color: black;

  &:hover {
    cursor: url("~assets/cursors/hand-steven.png"), auto;
  }
}

a.geert {
  &:hover {
    cursor: url("~assets/cursors/hand-geert.png"), auto;
  }
}

a.djenna {
  &:hover {
    cursor: url("~assets/cursors/hand-djenna.png"), auto;
  }
}

.section {
  &__wrapper {
    padding: 5rem 2.8rem 2rem 2.8rem;
    text-align: center;
  }
}

.block {
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
}

@media(min-width: $mq-l-laptop) {}
@media(min-width: $mq-xl-laptop) {}
@media(min-width: $mq-desktop) {}
</style>