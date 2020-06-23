<template>
  <div>
    <div class="section__wrapper">
      <div class="movie__holder" :class="author">
        <video controls>
          <source :src="movie" :alt="altMovie">
        </video>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    author: String,
    movie: String,
    altMovie: String,
  },
}
</script>
<style lang="scss" scoped>

  .movie__holder {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;

    &.sanne {
      background-color: $c-sanne-light;
    }

    &.steven {
      background-color: $c-steven;
    }

    &.geert {
      background-color: $c-geert-light;
    }

    &.djenna {
      background-color: $c-djenna-light;
    }
  }

  video {
    margin: 3rem 0;
    width: 80%;

    &:focus {
      outline: none;
    }
  }
  
  @media only screen and (min-width: $mq-tablet) {
    video {
      margin: 5rem 0;
      width: 70%;
    }
  }

  @media only screen and (min-width: $mq-s-laptop) {
    video { 
      margin: 7rem 0;
      width: 60%;
    }
  }

  @media only screen and (min-width: $mq-xl-laptop) {
    video {
      width: 55%;
    }
  }

  @media only screen and (min-width: $mq-desktop) {
    video {
      margin: 6rem 0;
      width: 48%;
    }
  }
</style>
