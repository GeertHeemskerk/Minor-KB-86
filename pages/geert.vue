<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <Profile
      image="/images/geert/profile.png"
      alt-image="Profiel foto"
    />
    <ProjectIntro
      author="geert"
      title= "Geert"
      text="Hi, mijn naam is Geert en ik ben 22 jaar. Tijdens mijn stage ben ik erachter gekomen dat het maken van statische websites zonder enige interactie vaak niet onthouden wordt. Aangezien wij op school tot nu toe alleen hebben geleerd hoe we een statische website moesten ontwerpen en coderen wilde ik meer uitdaging. Door mijn studie MBO applicatie ontwikkelaar heb ik veel kunnen leren over front &amp; back -end van een applicatie. Naast het ontwerpen en ontwikkelen van de applicatie wilde ik deze minor graag invullen met vakgebieden waar ik persoonlijk niet of nauwelijks kennis over heb, zodat ik later een breder visie heb over wat ik wil worden. Daarom heb ik de volgende vakgebieden benaderd in deze minor."
      subject="Rebranding - Webdesign - Cinema 4D - After Effects"
    />
    <BlockImage
      :image="require('~/assets/images/geert/redesign-webshop.png')"
      :image-loading="require('~/assets/images/geert/redesign-webshop.png?sqip')"
      alt-image="redesign webshop"
    />
    <BlockIntro
      author="geert"
      title="Blok 1"
      text="Aan het begin van de minor had ik nog bijna geen ervaring met Adobee Illustrator en Photoshop. In dit blok heb ik deze twee programma's samen met Figma (een prototype ontwerp systeem) een rebranding gemaakt van de Bijenkorf. De Bijenkorf heeft mij altijd al geïnspireerd door hun minimalistische aanpak en toch doordringende uistraling van hun website en campagnes. Ik dacht als ik een rebranding kan maken van de Bijenkorf die al aan de top staat van mijn lijst en ik daar tevreden over kan zijn is deze opdracht voor mij geslaagd. Daarnaast heb ik een volledige stylguide gemaakt en een herontwerp van de website op mijn minimalistische manier. Door de PDF te downloaden kunt u mijn ontwerpproces bekijken."
      link="/pdf/geert/17026121-Geert-Heemskerk-KB-86.pdf"
      link-text="download pdf"
    />
    <BlockImage      
      :image="require('~/assets/images/geert/redesign-front.png')"
      :image-loading="require('~/assets/images/geert/redesign-front.png?sqip')"
      alt-image="redesign front page"
    />
    <BlockImage
      :image="require('~/assets/images/geert/cards.png')"
      :image-loading="require('~/assets/images/geert/cards.png?sqip')"
      alt-image="card"
    />
    <BlokBlocks
      intro-text="In dit blok heb ik ook photoshop gebruikt en heb het gemaakt logo geplaatst op een tas van de Bijenkorf en deze bewerkt met kleuren en mijn idealen. Daarnaast heb ik zoals u hierboven kunt zien cadeaukaarten ontworpen die matchen met de styleguide van de website en principes van de Bijenkorf."
      author="geert"
      blok-image="/images/geert/shoppingbag.png"
      alt-image="shoppingbag"
    />
    <BlockIntro
      author="geert"
      title="Blok 2"
      text="In blok 1 werd ik geïnspireerd door klasgenoten en online voorbeelden van mockup animaties. Dit houdt in dat je een animatie afspeeld in een apparaat zoals een mobiele telefoon. Voor dit blok had ik nog nooit gewerkt met mockup animaties en 3D elementen. Hiervoor heb ik gebruikt gemaakt van C4D (Cinema 4D) en AAE (Adobe After Effects). De animatie die afspeeld op het scherm heb ik gemaakt in AAE. AAE en C4D heb ik binnen 5 weken moeten leren om tot dit eindresultaat te komen. Hiervoor heb ik in zo een korte tijd geleerd hoe ik materialen, licht, tijd, kijkhoeken, reflecties gebruik in C4D. Doordat ik C4D kon linken aan AEE kon ik makkelijk posities en animaties koppelen aan vereschillende soorten tijdstippen in het filmpje. Als u geïntresseerd ben in mijn werk kunt u mijn volledige ontwerpproces hieronder downloaden als PDF."
      link="/pdf/geert/17026121-Geert-Heemskerk-KB-86-3D-Animated.pdf"
      link-text="download pdf"
    />
    <MovieBlock
      author="geert"
      movie="/videos/geert/ScreenRecorded.mp4"
      alt-movie="shoppingbag"
    />
    <Footer
      author="geert"
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
import Footer from '~/components/Footer.vue';

export default {
  components: {
    Header,
    Profile,
    ProjectIntro,
    BlokBlocks,
    MovieBlock,
    BlockIntro,
    BlockImage,
    Footer,
  }
}
</script>
<style lang="scss" scoped>
.section__personal {
  cursor: url("~assets/cursors/cursor-geert.png"), auto;

  button, a {
    &:hover {
      cursor: url("~assets/cursors/hand-geert.png"), auto;
    }
  }
}
</style>
