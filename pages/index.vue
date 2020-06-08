<template>
  <main class="main">
    <Header />
    <section class="content">
      <h1 class="intro__title">SSDG</h1>
      <figure class="intro__figure">
        <img class="intro__media" src="~/assets/images/intro-image.png" alt="verf die samenkomt">
      </figure>
    </section>
  </main>
</template>

<script>
import Header from '~/components/Header.vue';
export default {
  components: {
    Header,
  }
}
</script>

<style scoped lang="scss">
.main {
  background-color: black; //TODO: USE VARIABLE
  width: 100vw;
  height: 100vh;
}
// .container {
//   margin: 0 auto;
//   min-height: 100vh;
//   display: flex;
//   justify-content: center;
//   align-items: center;
//   text-align: center;
// }

// .title {
//   font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
//     'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
//   display: block;
//   font-weight: 300;
//   font-size: 100px;
//   color: #35495e;
//   letter-spacing: 1px;
//   font-family: $f-heading;
// }

// .subtitle {
//   font-weight: 300;
//   font-size: 42px;
//   color: #526488;
//   word-spacing: 5px;
//   padding-bottom: 15px;
//   font-family: $f-heading;
// }

// .links {
//   padding-top: 15px;
// }
</style>
