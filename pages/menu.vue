<template>
  <div class="container">
    <div class="wrapper">
      <div class="menu_items">

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
    <div class="image-holder">
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


.image-holder {
  visibility: hidden;
  display: none;
}

@media only screen and (min-width: $mq-slaptop) {
  a {
    color: rgba($c-text, 0.5);
    text-decoration: none;
    display: block;
    margin: 2.5rem 0rem;
    font-family: $f-heading;
    font-size: 2rem;
    height: 2rem;
  }

  a:before {
    content: attr(data-text);
    color: $c-text;
    position: absolute;
    height: 0;
    overflow: hidden;
    transition: 0.6s;
    word-break: keep-all;

  }

  a:hover:before {
    height: 2.5rem;
  }

  .container {
    justify-content: center;
    align-items: left;
    text-align: left;
  }

  .wrapper{
    position: absolute;
    margin: 0rem 4.5rem;
    left: 0;
    z-index: 1;
  }

  .image-holder {
    position: absolute;
    visibility: visible;
    display: block;
    margin: 0rem 0rem 0rem 2rem;
  }

  img {
    box-shadow: inset 30px 0px 27px #000000
  }
}

@media only screen and (min-width: $mq-llaptop) {
  a {
    font-size: 2.4rem;
  }

  a:hover:before {
    height: 2.9rem;
  }

  .wrapper{
    margin: 0rem 5.5rem;
  }

  .image-holder {
    margin: 0rem 0rem 0rem 2rem;
  }
}

@media only screen and (min-width: $mq-desktop) {
  a {
    height: 4rem;
  }

  .wrapper{
    margin: 0rem 8.5rem;
  }

  .image-holder {
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
