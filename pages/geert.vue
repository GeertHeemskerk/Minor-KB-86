<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <ProjectIntro
    author="subcolor--geert"
    title= "Geert"
    text="Hi, mijn naam is Geert en ik ben 22 jaar. Tijdens mijn stage hoorde ik veel over 3D motion design en dit wekte intresse. Toen ik moest gaan zoeken naar een minor was ik dan ook druk opzoeken naar een 3D minor. Binnen Nederland kon ik hier niet veel over vinden. Tot ik hoorde dat er bij mij op school een pilot minor kwam waarin de leerlingen zelf mochten bepalen wat hun leerdoelen waren. In deze minor waren 4 blokken, en elk blok mocht anders worden ingevuld. In het eerste blok was dat voor mij natuurlijk 3D. Ik vond dit uiteindelijk zo leuk, dat ik van de minor een 3D minor heb gemaakt. Hier heb ik me dan ook de afgelopen 3 blokken op gefocust. De programma’s waarmee ik heb gewerkt zijn: "
    subject="Cinema 4D - After Effects"/>
    <BlokBlocks
      intro-text="In blok 3 ben ik opnieuw verder gegaan met 3D. Dit keer om meer te leren over texturen. Hier had ik nog niet veel mee gewerkt. Ik heb in dit blok gewerkt met UV-mapping en heb ook eigen texturen gemaakt door middel van foto’s bewerken. Het blad is een eigen gemaakte textuur."
      author="subcolor--geert"
      blok-image="/images/geert/shoppingbag.png"
      alt-image="shoppingbag"
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
  }
}
</script>
<style lang="scss" scoped>
</style>
