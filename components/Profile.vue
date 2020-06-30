<template>
  <section class="section__wrapper">
    <figure class="block__figure">
      <img class="block__media" :src="image" :alt="altImage">
    </figure>
    <div class="block__divider"></div>
  </section>
</template>
<script>
export default {
  props: {
    image: String,
    altImage: String
  }
}
</script>
<style lang="scss" scoped>

.section{
  &__wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

.block {
  &__divider {
    margin: 1rem auto;
    width: 2px;
    height: 1.2rem;
    background-color: black;
  }

  &__media {
    width: 100px;
    height: 100px;
  }
}

@media(min-width: $mq-tablet) {
  .block {
    &__media {
      width: 140px;
      height: 140px;
    }
  }
}

  @media(min-width: $mq-s-laptop) {
    .block {
      &__divider {
        height: 2.2rem;
      }
      &__media {
        width: 160px;
        height: 160px;
      }
    }
  }

  @media only screen and (min-width: $mq-xl-laptop) {
    .block {
      &__divider {
        margin: 2rem auto;
      }
      &__media {
        width: 180px;
        height: 180px;
      }
    }
  }

</style>
