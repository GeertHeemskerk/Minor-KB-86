<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <ProjectIntro
    author="subcolor--djenna"
    title= "Djenna"
    text="De minor Visual Design &amp; Front-end Development is in mijn ogen de perfecte minor geweest om volledig te focussen aan zelfontwikkeling binnen de opleiding.
    In de afgelopen jaren heb ik op school veel projecten en vakken mogen volgen, maar die mij niet allemaal evenveel interesseerde. Deze minor gaf mij de kans om zelf te bepalen wat ik nog wil leren en waar ik nog in wil groeien, zonder dat er een door school bedachten les achter zit. "
    subject="Logo’s ontwerpen - Animaties coderen"/>
    <BlokBlocks
      intro-text="In blok 2 wou ik meer leren over animeren. Ik wou een scene maken waarin verschillende animaties te zien zijn. Hier heb ik dit blok veel over geleerd, maar ook heb ik nog heel veel bij geleerd over modellen."
      author="subcolor--djenna"
      blok-image="/images/djenna/oog.png"
      alt-image="netlify"
    />
    <MovieBlock
    author="subcolor--djenna"
    movie="/images/djenna/examplevideo.png"
    alt-movie="examplevideo"
    />
  </section>
</template>
<script>
import Header from '~/components/Header.vue'
import ProjectIntro from '~/components/ProjectIntro.vue'
import BlokBlocks from '~/components/BlokBlocks.vue'
import MovieBlock from '~/components/MovieBlock.vue'

export default {
  components: {
    Header,
    ProjectIntro,
    BlokBlocks,
    MovieBlock
  }
}
</script>
<style lang="scss" scoped>

</style>
