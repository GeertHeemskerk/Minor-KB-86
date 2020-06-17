<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <BlockIntro
      author="sanne"
      title="Blok 1"
      text="Aan het begin van de minor had ik nog helemaal geen ervaring met 3D. Er is een 3D artist waar ik heel enthousiast van werd en dat is extraweg. Ik had hem een privebericht gestuurd op instagram en hij heeft mij een beetje opweg geholpen met welk programma ik het best kan gebruiken en wat uitleg gegeven over computer voor renderwerk. Hieruit kwam dat ik met Cinema 4D ging werken. Zij hebben ook een gratis studenten licentie. Ik ben hierna veel tutorials gaan kijken om het programma een beetje te leren kennen. Maar merkte ik al snel dat ik beter werk wanneer ik naar een doel toe werk. Toen heb ik mezelf als doel gesteld om een sushi band te maken. Hieronder is het eind resultaat te zien."
    />
    <BlockIntro
      author="sanne"
      title="Blok 3"
      text="In blok 3 ben ik opnieuw verder gegaan met 3D. Dit keer om meer te leren over texturen. Hier had ik nog niet veel mee gewerkt. Ik heb in dit blok gewerkt met UV-mapping en heb ook eigen texturen gemaakt door middel van foto’s bewerken. Het blad is een eigen gemaakte textuur."
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