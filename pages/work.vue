<template>
  <div class="container">

    <div class="menu_items">

    <nuxt-link to="/sanne"><h1>Sanne van Zeijl</h1></nuxt-link>
    <nuxt-link to="/steven"><h1>Steven Wu</h1></nuxt-link>
    <nuxt-link to="/djenna"><h1>Djenna Bakker</h1></nuxt-link>
    <nuxt-link to="/geert"><h1>Geert Heemskerk</h1></nuxt-link>

    </div>
  </div>
</template>

<script>
</script>

<style lang="scss">
.container {
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
  h1{
    margin: 2.5rem 0rem;
  }
}

a:hover {
  color: $c-text;
}

</style>
