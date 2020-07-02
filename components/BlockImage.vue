<template>
  <section class="section__wrapper" :class="{ 'section__wrapper--in-content' : !full }">
    <figure v-lazy-container="{ selector: 'img' }" class="block__figure">
      <img
        class="block__media"
        :data-src="image" 
        :data-loading="imageLoading" 
        :alt="altImage"
      />
    </figure>
  </section>
</template>
<script>
export default {
  props: {
    full: {
      type: Boolean,
      default: true
    },
    image: String,
    imageLoading: String,
    altImage: String
  }
}
</script>
<style lang="scss" scoped>
img[lazy='loading'] {
  filter: blur(1rem);
}

.section {
  &__wrapper {
    width: 100%;
    margin: 2rem 0;

    &--in-content {
      padding: 0rem 2.8rem;
    }
  }
}

.block {
  &__figure {
    width: 100%;
  }

  &__media {
    width: 100%;
    height: auto;
  }
}

@media(min-width: $mq-tablet) {
  .section {
    &__wrapper {
      &--in-content {
        padding-left: 4rem;
        padding-right: 4rem;
      }
    }
  }
}

@media(min-width: $mq-s-laptop) {
  .section {
    &__wrapper {
      margin: 3rem 0;

      &--in-content {
        max-width: 1030px;
        margin: 3rem auto; 
      }
    }
  }
}

@media(min-width: $mq-l-laptop) {}
@media(min-width: $mq-xl-laptop) {}
@media(min-width: $mq-desktop) {}
</style>