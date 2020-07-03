<template>
  <section class="section__wrapper" :class="author">
    <div class="gallery">
      <figure class="gallery__figure" v-lazy-container="{ selector: 'img' }" v-for="(img, index) in images" :key="index">
        <img 
          class="gallery__media"
          :data-src="img.src" 
          :data-loading="img.srcLoading" 
          :alt="img.alt">
      </figure>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    author: String,
    images: Array
  }
}
</script>
<style lang="scss" scoped>

section.sanne {
  background-color: $c-sanne;
}

section.steven {
  background-color: $c-steven;
}

section.geert {
  background-color: $c-geert;
}

section.djenna {
  background-color: $c-djenna;
}

.section {
  &__wrapper {
    width: 100%;
  }
}

.gallery {
  margin: 0 auto;
  padding: 5rem 0;
  width: 80%;

  &__figure {
    width: 100%;
    margin-bottom: 1rem;

    &:last-child {
      padding-bottom: 0;
    }
  }

  &__media {
    width: 100%;
    height: auto;
  }
}

@media(min-width: $mq-tablet) {
  .gallery {
    width: 70%;
  }
}

@media(min-width: $mq-s-laptop) {
  .gallery {
    width: 60%;
  }
}

@media(min-width: $mq-l-laptop) {
  .gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;

    &__figure {
      flex: 1 0 49%;
      max-width: 49%;
      margin-bottom: .8rem;
    }
  }
}

@media(min-width: $mq-xl-laptop) {
  .gallery {
    width: 55%;

    &__figure {
      flex: 1 0 47%;
      max-width: 47%;
      margin-bottom: 3rem;
    }
  }
}  
</style>