<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
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

export default { 
  components: {
    Header,
    BlockIntro,
  }
}
</script>
<style lang="scss" scoped>

</style>