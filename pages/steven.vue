<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <ProjectIntro
    author="subcolor--steven"
    title= "Steven"
    text="Visual Design &amp; Front-end Development is een minor die goed bij mijn interesses aansluit. Binnen deze minor ben je gefocust op jezelf ontwikkelen en leer wat je graag wilt leren. Hi, mijn is Steven en ik ben CMD-student met liefde voor Front-end development. Ik wil graag mezelf verder ontwikkelen in het gebied van design en development en daarom is perfect voor mij. Deze minor is verdeeld in 4 blokken van 5 weken en elk blok mag je zelf een leerdoel kiezen en dit mag van alles zijn in het gebied van visual design en front-end development. Ik heb gekozen om in de eerste blok design te doen en de resterende blok heb ik gekozen om mijn development skills in praktijk te zetten."
    subject="Applicatie - Wordpress Thema - JamStack"/>
    <BlokBlocks
      intro-text="Tijdens een masterclass van onze minor heeft een van onze docenten over JAMstack gehad, een techniek die in laatste jaren veel wordt gebruikt om website te bouwen. De prestatie van de website vergeleken met andere website is heel hoog. Dus ik wou in dit blok zelf een website maken in JAMstack."
      author="subcolor--steven"
      blok-image="/images/steven/netlify.png"
      alt-image="netlify image"
    />
  </section>
</template>
<script>
import Header from '~/components/Header.vue'
import ProjectIntro from '~/components/ProjectIntro.vue'
import BlokBlocks from '~/components/BlokBlocks.vue'

export default {
  components: {
    Header,
    ProjectIntro,
    BlokBlocks
  },
}
</script>
<style lang="scss" scoped>

</style>
