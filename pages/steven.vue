<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <ProjectIntro
      author="subcolor--steven"
      title= "Steven"
      text="Visual Design &amp; Front-end Development is een minor die goed bij mijn interesses aansluit. Binnen deze minor ben je gefocust op jezelf ontwikkelen en leer wat je graag wilt leren. Hi, mijn is Steven en ik ben CMD-student met liefde voor Front-end development. Ik wil graag mezelf verder ontwikkelen in het gebied van design en development en daarom is perfect voor mij. Deze minor is verdeeld in 4 blokken van 5 weken en elk blok mag je zelf een leerdoel kiezen en dit mag van alles zijn in het gebied van visual design en front-end development. Ik heb gekozen om in de eerste blok design te doen en de resterende blok heb ik gekozen om mijn development skills in praktijk te zetten."
      subject="Applicatie - Wordpress Thema - JamStack"
    />
    <BlockIntro
      author="steven"
      title="Blok 1"
      text="In dit blok ga ik de OSIRIS dashboard van de Haagse Hogeschool herontwerpen in Figma, een ontwerp programma. Ik heb nooit ontwerp gemaakt van een dashboard dus eerst heb ik in wat theorieën gedoken over het ontwerpen van dashboard. Vervolgens heb ik inspiraties gezocht op dashboard designs. Deze inspiraties gaf me een idee hoe ik de layout van de dashboard moet opstellen."
    />
    <BlockIntro
      author="steven"
      title="Blok 2"
      text="In blok 2 heb ik gekozen om richting front-end development te gaan. Tijdens mijn stage heb ik veel geleerd over Wordpress en thema maken. Daarmee wil ik verder gaan dus ik heb gekozen om een thema te maken van scratch voor onze minor website in Wordpress. Voor dit blok gebruik ik Wordpress, ACF en Timber om mijn thema te bouwen."
    />
    <BlokBlocks
      intro-text="Tijdens een masterclass van onze minor heeft een van onze docenten over JAMstack gehad, een techniek die in laatste jaren veel wordt gebruikt om website te bouwen. De prestatie van de website vergeleken met andere website is heel hoog. Dus ik wou in dit blok zelf een website maken in JAMstack."
      author="subcolor--steven"
      blok-image="/images/steven/netlify.png"
      alt-image="netlify image"
    />
    <BlockIntro
      author="steven"
      title="Blok 3"
      text="Er zijn verschillende tools die je kan gebruiken voor het implementatie van JAMstack, ik heb gekozen om met Nuxt.js een framework van Vue en DatoCMS te gebruiken als CMS. Vroeger heb ik een paar cursussen van Vue.js gevolgd. Voor de ontwerp ik gekozen om de website van mijn vorige blok te gebruiken. Hierdoor besteed ik dus meer tijd in de technieken dan in het layout van de website."
    />
  </section>
</template>
<script>
import Header from '~/components/Header.vue';
import BlockIntro from '~/components/BlockIntro.vue';
import ProjectIntro from '~/components/ProjectIntro.vue';
import BlokBlocks from '~/components/BlokBlocks.vue';

export default {
  components: {
    Header,
    ProjectIntro,
    BlokBlocks,
    BlockIntro,
  },
}
</script>
<style lang="scss" scoped>

</style>
