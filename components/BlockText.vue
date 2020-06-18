<template>
  <div class="section__wrapper">
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
    text: String,
    link: String,
    linkText: String
  }
}
</script>
<style lang="scss" scoped>

a.sanne {
  color: $c-sanne;
}


a.steven {
  color: $c-steven-darker;
}


a.geert {
  color: $c-geert;
}


a.djenna {
 color: $c-djenna;
}

.section {
  &__wrapper {
    padding: 5rem 2.8rem 2rem 2.8rem;
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
}

@media(min-width: $mq-l-laptop) {}

@media(min-width: $mq-xl-laptop) {}

@media(min-width: $mq-desktop) {}

</style>