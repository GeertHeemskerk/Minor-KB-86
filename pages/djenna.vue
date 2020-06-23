<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <ProjectIntro
      author="subcolor--djenna"
      title= "Djenna"
      text="De minor Visual Design &amp; Front-end Development is in mijn ogen de perfecte minor geweest om volledig te focussen aan zelfontwikkeling binnen de opleiding. In de afgelopen jaren heb ik op school veel projecten en vakken mogen volgen, maar die mij niet allemaal evenveel interesseerde. Deze minor gaf mij de kans om zelf te bepalen wat ik nog wil leren en waar ik nog in wil groeien, zonder dat er een door school bedachten les achter zit. "
      subject="Logo’s ontwerpen - Animaties coderen"
    />
    <MovieBlock
      author="subcolor--djenna"
      movie="/images/djenna/examplevideo.png"
      alt-movie="examplevideo"
    />
    <BlockIntro
      author="djenna"
      title="Blok 1"
      text="Voor het eerste blok van deze minor heb ik gekomen om logo’s te maken en meer leren over de theorie en technieken erachter. Eerst ben ik op zoek gegaan naar verschillende theorieën en trend bij het maken van logo’s. Er waren veel regels die ik nog niet wist over het maken, zoals bijvoorbeeld kleurgebruik, positie en betekenis. Met deze nieuwe kennis heb ik, naar mijn mening, veel betere logo’s kunnen maken. Mijn deliverables voor dit blok was het volgen van tutorials inclusief de uitwerkingen ervan en het vijf uitgewerkte logo’s."
    />
    <BlokBlocks
      intro-text="In blok 2 wou ik meer leren over animeren. Ik wou een scene maken waarin verschillende animaties te zien zijn. Hier heb ik dit blok veel over geleerd, maar ook heb ik nog heel veel bij geleerd over modellen."
      author="subcolor--djenna"
      blok-image="/images/djenna/oog.png"
      alt-image="netlify"
    />
    <BlockIntro
      author="djenna"
      title="Blok 2"
      text="Ik merkte in blok 2 dat er nog veel meer over animaties te leren viel, maar dat ik er toen niet genoeg tijd voor had. Daardoor heb ik de keuze gemaakt om verder te gaan met het leren coderen van animaties voor op websites, zodat ik mijn kennis nog meer kan verbreden en dus nog veel meer kan leren over dit onderwerp. Ik had het doel om aan de website van het vorige doel een aantal animaties toe te voegen, met de focus op moeilijkere animaties dan bij het vorige blok. Om mezelf echt verder te kunnen ontwikkelen, moest ik op een niveau hoger gaan werken. De deliverables voor dit blok waren het volgen van tutorials inclusief mogelijke uitwerkingen en drie animaties toevoegen aan de website."
    />
    <BlockImage
      :full="false"
      image="/images/djenna/landingpage-porfolio.png"
      alt-image="landingpage pagina"
    />
    <BlockVideo
      :full="false"
      video="/images/djenna/landingpage-porfolio.png"
    />
    <BlockIntro
      author="djenna"
      title="Blok 3"
      text="Ik merkte in blok 2 dat er nog veel meer over animaties te leren viel, maar dat ik er toen niet genoeg tijd voor had. Daardoor heb ik de keuze gemaakt om verder te gaan met het leren coderen van animaties voor op websites, zodat ik mijn kennis nog meer kan verbreden en dus nog veel meer kan leren over dit onderwerp. Ik had het doel om aan de website van het vorige doel een aantal animaties toe te voegen, met de focus op moeilijkere animaties dan bij het vorige blok. Om mezelf echt verder te kunnen ontwikkelen, moest ik op een niveau hoger gaan werken. De deliverables voor dit blok waren het volgen van tutorials inclusief mogelijke uitwerkingen en drie animaties toevoegen aan de website."
    />
    <Footer
      author="subcolor--djenna"
    />
  </section>
</template>
<script>
import Header from '~/components/Header.vue';
import BlockIntro from '~/components/BlockIntro.vue';
import BlokBlocks from '~/components/BlokBlocks.vue';
import ProjectIntro from '~/components/ProjectIntro.vue';
import MovieBlock from '~/components/MovieBlock.vue';
import BlockImage from '~/components/BlockImage.vue';
import BlockVideo from '~/components/BlockVideo.vue';
import Footer from '~/components/Footer.vue';

export default {
  components: {
    Header,
    ProjectIntro,
    BlokBlocks,
    MovieBlock,
    BlockIntro,
    BlockImage,
    BlockVideo,
    Footer,
  }
}
</script>
<style lang="scss" scoped>

</style>
