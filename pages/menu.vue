<template>
  <div class="container">
    <div class="container__wrapper">
      <div class="menu__items">
        <nuxt-link to="/sanne" data-text="Sanne van Zeijl">
          Sanne van Zeijl
        </nuxt-link>
        <nuxt-link to="/steven" data-text="Steven Wu">
          Steven Wu
        </nuxt-link>
        <nuxt-link to="/" data-text="KB-86 SSDG">
          KB-86 SSDG
        </nuxt-link>
        <nuxt-link to="/djenna" data-text="Djenna Bakker">
          Djenna Bakker
        </nuxt-link>
        <nuxt-link to="/geert" data-text="Geert Heemskerk">
          Geert Heemskerk
        </nuxt-link>
      </div>
    </div>
    <div class="image__holder">
      <figure>
        <img id="sanne" src="~/assets/images/imgTest.png" alt="imgTest">
      </figure>
      <!-- <figure>
        <img id="steven" src="~/assets/images/imgTest.png" alt="imgTest">
      </figure>
      <figure>
        <img id="kb" src="~/assets/images/imgTest.png" alt="imgTest">
      </figure>
      <figure>
        <img id="djenna" src="~/assets/images/imgTest.png" alt="imgTest">
      </figure>
      <figure>
        <img id="geert" src="~/assets/images/imgTest.png" alt="imgTest">
      </figure> -->
    </div>
  </div>
</template>
<script>
export default {
  
}
</script>

<style scoped lang="scss">
.container {
  position: relative;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: $c-background;
}

a {
  color: rgba($c-text, 0.5);
  text-decoration: none;
  display: block;
  margin: 2.5rem 0rem;
  font-family: $f-heading;
  font-size: 1.6rem;
}

.image__holder {
  visibility: hidden;
  display: none;
}

@media only screen and (min-width: $mq-s-laptop) {
  img {
    transition: 1.3s;
    opacity: 0;
    transform: scale(0.8)
  }

  img:hover{
    animation: zoomIn 1.3s;
    opacity: 1;
    transform: scale(1.0);
  }

  a {
    font-size: 2rem;
    height: 2rem;
  }

  a:before {
    content: attr(data-text);
    color: $c-text;
    position: absolute;
    height: 0;
    overflow: hidden;
    transition: 0.8s;
    word-break: keep-all;
  }

  a:hover:before {
    height: 2.5rem;
  }

  .container {
    justify-content: center;
    align-items: left;
    text-align: left;

    &__wrapper {
      position: absolute;
      margin: 0rem 4.5rem;
      left: 0;
      z-index: 1;
    }
  }

  .image__holder {
    position: absolute;
    visibility: visible;
    display: block;
    margin: 0rem 0rem 0rem 2rem;
  }
}

@media only screen and (min-width: $mq-l-laptop) {
  a {
    font-size: 2.4rem;
  }

  a:hover:before {
    height: 2.9rem;
  }

  .container {
    &__wrapper {
      margin: 0rem 5.5rem;
    }
  }

  .image__holder {
    margin: 0rem 0rem 0rem 2rem;
  }
}

@media only screen and (min-width: $mq-desktop) {
  a {
    height: 4rem;
  }

  .container {
    &__wrapper {
      margin: 0rem 8.5rem;
    }
  }

  .image__holder {
    width: 1240px;
    height: auto;
    margin: 0rem;
  }

  figure, img {
    width: 100%;
    height: 100%;
  }
}
</style>
