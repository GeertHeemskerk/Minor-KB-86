<template>
  <section class="section__wrapper" :class="author">
    <section class="gallery">
      <figure class="gallery__figure" v-lazy-container="{ selector: 'img' }" v-for="(img, index) in logos" :key="index">
        <img 
          class="gallery__media"
          :data-src="img.src" 
          :data-loading="img.srcLoading" 
          :alt="img.alt">
      </figure>
    </section>
  </section>
</template>
<script>
export default {
  props: {
    author: String,
    logos: Array,
  }
}
</script>
<style lang="scss" scoped>

.section {
  &__wrapper {
    width: 100%;

    &.sanne {
      background-color: $c-sanne-light;
    }

    &.steven {
      background-color: $c-steven-light;
    }

    &.geert {
      background-color: $c-geert-light;
    }

    &.djenna {
      background-color: $c-djenna-light;
    }
  }
}

.gallery {
  width: 90%;
  margin: 0rem auto;
  padding: 2rem 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  max-width: 820px;
  align-items: center;

  &__figure {
    flex: 1 0 26%;
    max-width: 26%;
  }

  &__media {
    width: 100%;
    height: auto
  }
}
</style>