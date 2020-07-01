<template>
  <div class="section__wrapper">
    <h2 class="block__title" :class="author">{{ title }}</h2>
    <div class="block__divider"></div>
    <p class="block__text">{{ text }}</p>
    <a class="block__link" :class="author" v-if="link" :href="link" target="_blank">
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

h2.sanne, a.sanne {
  color: $c-sanne;
}

h2.steven, a.steven {
  color: $c-steven-darker;
}

h2.geert, a.geert {
  color: $c-geert;
}

h2.djenna, a.djenna {
 color: $c-djenna;
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

.section {
  &__wrapper {
    padding: 5rem 2.8rem 2rem 2.8rem;
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