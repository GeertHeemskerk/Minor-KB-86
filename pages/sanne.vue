<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <Profile
      :image="require('~/assets/images/sanne/profile.png')"
      :image-loading="require('~/assets/images/sanne/profile.png?lqip')"
      alt-image="Profiel foto van sanne"
    />
    <ProjectIntro
      author="sanne"
      title= "Sanne"
      text="Hi, mijn naam is Sanne en ik ben 22 jaar. Tijdens mijn stage hoorde ik veel over 3D motion design en dit wekte intresse. Toen ik moest gaan zoeken naar een minor was ik dan ook druk opzoeken naar een 3D minor. Binnen Nederland kon ik hier niet veel over vinden. Tot ik hoorde dat er bij mij op school een pilot minor kwam waarin de leerlingen zelf mochten bepalen wat hun leerdoelen waren. In deze minor waren 4 blokken, en elk blok mocht anders worden ingevuld. In het eerste blok was dat voor mij natuurlijk 3D. Ik vond dit uiteindelijk zo leuk, dat ik van de minor een 3D minor heb gemaakt. Hier heb ik me dan ook de afgelopen 3 blokken op gefocust. De programma’s waarmee ik heb gewerkt zijn: "
      subject="Cinema 4D - After Effects"
    />
    <BlockImage
      :image="require('~/assets/images/sanne/intro-block-image.png')"
      :image-loading="require('~/assets/images/sanne/intro-block-image.png?lqip')"
      alt-image="3d render model face"
    />
    <BlockIntro
      author="sanne"
      title="Blok 1"
      text="Aan het begin van de minor had ik nog helemaal geen ervaring met 3D. Er is een 3D artist waar ik heel enthousiast van werd en dat is extraweg. Ik had hem een privebericht gestuurd op instagram en hij heeft mij een beetje opweg geholpen met welk programma ik het best kan gebruiken en wat uitleg gegeven over computer voor renderwerk. Hieruit kwam dat ik met Cinema 4D ging werken. Zij hebben ook een gratis studenten licentie. Ik ben hierna veel tutorials gaan kijken om het programma een beetje te leren kennen. Maar merkte ik al snel dat ik beter werk wanneer ik naar een doel toe werk. Toen heb ik mezelf als doel gesteld om een sushi band te maken. Hieronder is het eind resultaat te zien."
    />
    <BlockVideo
      :full="false"
      video="/videos/sanne/sushi-table-animation.mp4"
    />
    <BlockIntro
      author="sanne"
      title="Blok 2"
      text="In blok 2 wou ik meer leren over animeren. Ik wou een scene maken waarin verschillende animaties te zien zijn. Hier heb ik dit blok veel over geleerd, maar ook heb ik nog heel veel bij geleerd over modellen."
    />
    <BlokBlocks
      intro-text="Hiernaast is te zien hoe ik de scene er buiten de camera uitziet. De groene lijnen zijn het gezichtsveld van de camera, en die beweegt door de gang heen naar het eind. Hierin gebeuren dus verschillende animaties en zie je verschillende objecten. Hieronder is het eindresultaat te zien."
      author="sanne"
      :blok-image="require('~/assets/images/sanne/c4d.png')"
      :blok-image-loading="require('~/assets/images/sanne/c4d.png?lqip')"
      alt-image="c4d"
    />
    <MovieBlock
      author="sanne"
      movie="/videos/sanne/rendervideo.mp4"
      alt-movie="examplevideo"
    />
    <BlockIntro
      author="sanne"
      title="Blok 3"
      text="In blok 3 ben ik opnieuw verder gegaan met 3D. Dit keer om meer te leren over texturen. Hier had ik nog niet veel mee gewerkt. Ik heb in dit blok gewerkt met UV-mapping en heb ook eigen texturen gemaakt door middel van foto’s bewerken. Het blad is een eigen gemaakte textuur."
    />
    <Triplets
      :left="require('~/assets/images/sanne/left.png')"
      :left-loading="require('~/assets/images/sanne/left.png?lqip')"
      left-alt="render of 3d eye"
      :middle="require('~/assets/images/sanne/middle.png')"
      :middle-loading="require('~/assets/images/sanne/middle.png?lqip')"
      middle-alt="render of 3d face"
      :right="require('~/assets/images/sanne/right.png')"
      :right-loading="require('~/assets/images/sanne/right.png?lqip')"
      right-alt="render of 3d lips"
    />
    <Footer
      author="sanne"
    />
  </section>
</template>
<script>
import Header from '~/components/Header.vue';
import Profile from '~/components/Profile.vue';
import BlockIntro from '~/components/BlockIntro.vue';
import ProjectIntro from '~/components/ProjectIntro.vue';
import BlokBlocks from '~/components/BlokBlocks.vue';
import MovieBlock from '~/components/MovieBlock.vue';
import BlockImage from '~/components/BlockImage.vue';
import BlockVideo from '~/components/BlockVideo.vue';
import Triplets from '~/components/Triplets.vue';
import Footer from '~/components/Footer.vue';

export default {
  components: {
    Header,
    Profile,
    ProjectIntro,
    MovieBlock,
    BlockIntro,
    BlockImage,
    BlockVideo,
    BlokBlocks,
    Triplets,
    Footer,
  }
}
</script>
<style lang="scss" scoped>
.section__personal {
  cursor: url("~assets/cursors/cursor-sanne.png"), auto;

  button, a {
    &:hover {
      cursor: url("~assets/cursors/hand-sanne.png"), auto;
    }
  }
}
</style>
