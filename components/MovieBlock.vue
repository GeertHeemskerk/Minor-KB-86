<template>
  <div>
    <div class="section__wrapper">
      <div class="movie__holder" :class="author">
        <img :src="movie" :alt="altMovie">
      </div>
    </div>
  </div>
</template>
<script>
import Icons from '~/components/Icons.vue';

export default {
  components: {

  },
  props: {
    author: String,
    movie: String,
    altMovie: String,
  }
}
</script>
<style lang="scss" scoped>

  .movie__holder{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 380px;
  }

  img {
    width: 80%;
    height: 50%;
  }

  .subcolor--steven {
    background-color: $c-steven;
  }

  .subcolor--sanne {
    background-color: $c-sanne-light;
  }

  .subcolor--geert {
    background-color: $c-geert-light;
  }

  .subcolor--djenna {
    background-color: $c-djenna-light;
  }

  @media only screen and (min-width: $mq-tablet) {
    .movie__holder{
      width: 100%;
      height: 400px;
    }

    img {
      width: 70%;
      height: 70%;
    }
  }

  @media only screen and (min-width: $mq-s-laptop) {
    img {
      width: 60%;
      height: 75%;
    }
  }

  @media only screen and (min-width: $mq-xl-laptop) {
    .movie__holder{
      width: 100%;
      height: 550px;
    }

    img {
      width: 55%;
      height: 80%;
    }
  }

  @media only screen and (min-width: $mq-desktop) {
    .movie__holder{
      width: 100%;
      height: 750px;
    }

    img {
      width: 55%;
      height: 80%;
    }
  }
</style>
