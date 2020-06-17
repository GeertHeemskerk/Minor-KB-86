<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <ProjectIntro
    author="subcolor--djenna"
    title= "Djenna"
    text="De minor Visual Design &amp; Front-end Development is in mijn ogen de perfecte minor geweest om volledig te focussen aan zelfontwikkeling binnen de opleiding.
    In de afgelopen jaren heb ik op school veel projecten en vakken mogen volgen, maar die mij niet allemaal evenveel interesseerde. Deze minor gaf mij de kans om zelf te bepalen wat ik nog wil leren en waar ik nog in wil groeien, zonder dat er een door school bedachten les achter zit. "
    subject="Logo’s ontwerpen - Animaties coderen"/>
  </section>
</template>
<script>
import Header from '~/components/Header.vue'
import ProjectIntro from '~/components/ProjectIntro.vue'

export default {
  components: {
    Header,
    ProjectIntro
  }
}
</script>
<style lang="scss" scoped>

</style>
