<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <Profile
      :image="require('~/assets/images/djenna/profile.png')"
      :image-loading="require('~/assets/images/djenna/profile.png?lqip')"
      alt-image="Profiel foto van djenna"
    />
    <ProjectIntro
      author="djenna"
      title= "Djenna"
      text="De minor Visual Design &amp; Front-end Development is in mijn ogen de perfecte minor geweest om volledig te focussen aan zelfontwikkeling binnen de opleiding. In de afgelopen jaren heb ik op school veel projecten en vakken mogen volgen, maar die mij niet allemaal evenveel interesseerde. Deze minor gaf mij de kans om zelf te bepalen wat ik nog wil leren en waar ik nog in wil groeien, zonder dat er een door school bedachten les achter zit. "
      subject="Logo’s ontwerpen - Animaties coderen"
    />
    <MovieBlock
      author="djenna"
      movie="/videos/djenna/preloader.mov"
      alt-movie="preloader"
    />
    <BlockIntro
      author="djenna"
      title="Blok 1"
      text="Voor het eerste blok van deze minor heb ik gekomen om logo’s te maken en meer leren over de theorie en technieken erachter. Eerst ben ik op zoek gegaan naar verschillende theorieën en trend bij het maken van logo’s. Er waren veel regels die ik nog niet wist over het maken, zoals bijvoorbeeld kleurgebruik, positie en betekenis. Met deze nieuwe kennis heb ik, naar mijn mening, veel betere logo’s kunnen maken. Mijn deliverables voor dit blok was het volgen van tutorials inclusief de uitwerkingen ervan en het vijf uitgewerkte logo’s."
    />
    <BlockImage
      :image="require('~/assets/images/djenna/logotypefaces.png')"
      :image-loading="require('~/assets/images/djenna/logotypefaces.png?lqip')"
      alt-image="landingpage pagina"
    />
    <BlockText
      author="djenna"
      text="Ik heb uiteindelijk vijf logo’s gemaakt, twee daarvan waren voor echte bedrijven en de andere drie waren voor fictieve bedrijven. Als ik weet voor wat voor bedrijf ik een logo moet maken, waar zij voor staan en wat zij willen uitstralen,
      is het voor mij voor makkelijker om daarmee aan de slag te gaan. Uiteindelijk ben ik super trots op de logo’s die ik gemaakt heb, en de twee bedrijven wa  arvoor ik logo’s maakte waren er ook blij en tevreden mee."
    />
    <BlockImage
      :full="false"
      :image="require('~/assets/images/djenna/logos.png')"
      :image-loading="require('~/assets/images/djenna/logos.png?lqip')"
      alt-image="landingpage pagina"
    />
    <BlockIntro
      author="djenna"
      title="Blok 2"
      text="Een ander leerdoel van mij was om te leren hoe ik animatie kan coderen, met name voor op websites. Ik vind coderen heel leuk, maar ik heb nog heel veel om te leren binnen het vak. Een van deze dingen zijn animaties, oftewel bewegende elementen op een pagina, heeft mij altijd al geïnteresseerd en aangesproken. Dit kan bijvoorbeeld tekst zijn die binnen komt vallen, een animatie die laat zien dat iets aan het laden is, of een bewegende achtergrond. In de afgelopen schooljaren is er weinig tijd voor geweest om deze stof te leren, en deze minor was het perfecte moment om hier meer over te leren. Mijn deliverables voor dit blok was een onderzoeksportfolio, tutorials inclusief uitwerkingen en een website met animaties erop."
    />
    <BlokBlocks
      intro-text="Op Skillshare vond ik een tutorial waar animaties gemaakt werden met pure CSS. Dit was voor mij goed om te beginnen, omdat het best makkelijk is om animaties te maken met CSS en het niet altijd nodig is om animaties te maken in JavaScript. Met het oog had ik het zwarte gedeelte geanimeerd, waardoor het leek alsof het oog naar dingen keek."
      author="djenna"
      blok-video="/videos/djenna/oog.mov"
    />
    <BlockText
      author="djenna"
      text="Omdat ik nog geen voorkennis van animaties, heb ik tientallen tutorials gevolgd om van alles te leren over animaties. Zowel over de geschiedenis van animaties, hoe animaties geëvalueerd zijn en hoe ze nu gebruikt worden op websites. Ik heb vervolgens een simpel design gemaakt voor een portfolio achtige website, waar ik dan uiteindelijk animaties op kon plaatsen. Met deze website heb ik kunnen bewijzen hoeveel ik geleerd heb in dat blok en hoe ik deze geïmplementeerd heb op een website."
      link="https://djennabakker.github.io/codes/"
      link-text="Bekijk de website"
      link-title="Ga naar de animatie website van Djenna"
    />
    <BlockVideo
      :full="false"
      video="/videos/djenna/hero-sectie.mov"
    />
    <BlockVideo
      :full="false"
      video="/videos/djenna/work-sectie.mov"
    />
    <BlockVideo
      :full="false"
      video="/videos/djenna/about-me-contact-secties.mov"
    />
    <BlockIntro
      author="djenna"
      title="Blok 3"
      text="Ik merkte in blok 2 dat er nog veel meer over animaties te leren viel, maar dat ik er toen niet genoeg tijd voor had. Daardoor heb ik de keuze gemaakt om verder te gaan met het leren coderen van animaties voor op websites, zodat ik mijn kennis nog meer kan verbreden en dus nog veel meer kan leren over dit onderwerp. Ik had het doel om aan de website van het vorige doel een aantal animaties toe te voegen, met de focus op moeilijkere animaties dan bij het vorige blok. Om mezelf echt verder te kunnen ontwikkelen, moest ik op een niveau hoger gaan werken. De deliverables voor dit blok waren het volgen van tutorials inclusief mogelijke uitwerkingen en drie animaties toevoegen aan de website."
    />
    <MovieBlock
      author="djenna"
      movie="/videos/djenna/preloader.mov"
      alt-movie="preloader"
    />
    <BlockText
      author="djenna"
      text="Mijn doel was om een laadscherm te animeren, dus wanneer iemand op de website komt ziet hij eerst een laadscherm terwijl de hele pagina wordt ingeladen. Daarna wilde ik een grote achtergrond animatie toevoegen, maar ik kon geen tutorial vinden voor een animatie die toegevoegde waarde aan de website zou geven. Dus in plaats daarvan heb ik een aan de eerste sectie een typemachine animatie toegevoegd, waarmee ik de gebruiker begroet met verschillende termen. Tot slot wilde ik graag de progressie balken animeren, zodat ze van 0% naar het desbetreffende percentage zouden ‘schuiven’. Met behulp van een docent is dit uiteindelijk goed gelukt!"
      link="https://djennabakker.github.io/code/"
      link-text="Bekijk de website"
      link-title="Ga naar de animatie website van Djenna"
    />
    <BlockVideo
      :full="false"
      video="/videos/djenna/typewriter-animation.mov"
    />
    <BlockVideo
      :full="false"
      video="/videos/djenna/progress-bar-animatie.mov"
    />
    <Footer
      author="djenna"
    />
  </section>
</template>
<script>
import Header from '~/components/Header.vue';
import Profile from '~/components/Profile.vue';
import BlockIntro from '~/components/BlockIntro.vue';
import BlokBlocks from '~/components/BlokBlocks.vue';
import ProjectIntro from '~/components/ProjectIntro.vue';
import MovieBlock from '~/components/MovieBlock.vue';
import BlockImage from '~/components/BlockImage.vue';
import BlockVideo from '~/components/BlockVideo.vue';
import Footer from '~/components/Footer.vue';
import BlockText from '~/components/BlockText.vue';

export default {
  components: {
    Header,
    Profile,
    ProjectIntro,
    BlokBlocks,
    MovieBlock,
    BlockIntro,
    BlockImage,
    BlockVideo,
    Footer,
    BlockText,
  }
}
</script>
<style lang="scss" scoped>
  .section__personal {
    cursor: url("~assets/cursors/cursor-djenna.png"), auto;

    button, a {
      &:hover {
        cursor: url("~assets/cursors/hand-djenna.png"), auto;
      }
    }
  }
</style>
