<template>
  <div>
    <div :class="author" class="section__wrapper">
      <h1 :class="author" >KB-86</h1>
      <nuxt-link :class="author" to="/sanne">
        Sanne
      </nuxt-link>
      <nuxt-link  :class="author" to="/steven">
        Steven
      </nuxt-link>
      <nuxt-link :class="author" to="/djenna">
        Djenna
      </nuxt-link>
      <nuxt-link :class="author" to="/geert">
        Geert
      </nuxt-link>
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
  }
}
</script>
<style lang="scss" scoped>

  .section__wrapper {
    text-align: center;
    width: 100%;
    padding: 2rem;
  }

  a, h1{
    color: white;
    text-decoration: none;
  }

  h1 {
    font-size: 3rem;
    margin: 0 0 2rem 0;
  }

  a {
    margin: 0 0.2rem;
  }

  h1.subcolor--steven {
   color: black;
  }

  a.subcolor--steven {
   color: black;
  }

  .subcolor--steven {
    background-color: $c-steven;
  }

  .subcolor--sanne {
    background-color: $c-sanne;
  }

  .subcolor--geert {
    background-color: $c-geert;
  }

  .subcolor--djenna {
    background-color: $c-djenna;
  }

  @media only screen and (min-width: $mq-tablet) {
    .section__wrapper {
      padding: 4rem;
    }

    h1 {
      font-size: 4rem;
      margin: 0 0 2rem 0;
    }

    a {
      margin: 0 2rem;
    }
  }
</style>
