<template>
  <section class="section__personal">
    <Header class-name="header--personal" />
    <Profile
      :image="require('~/assets/images/steven/profile.png')"
      :image-loading="require('~/assets/images/steven/profile.png?lqip')"
      alt-image="Profiel foto van steven"
    />
    <ProjectIntro
      author="steven"
      title="Steven"
      text="Visual Design &amp; Front-end Development is een minor die goed aan mijn interesses sluit. Binnen deze minor ben je gefocust op zelfontwikkeling. Hi, mijn naam is Steven en ik ben CMD-student met liefde voor Front-end development. Ik wil graag mezelf verder ontwikkelen in het gebied van design en development en daarom is deze minor perfect voor mij. Deze minor is verdeeld in 4 blokken van 5 weken en elk blok mag je zelf een leerdoel kiezen. Dit mag van alles zijn binnen het gebied van visual design en front-end development. Ik heb gekozen om in de eerste blok design te ontwerpen en de resterende blok heb ik gekozen om mijn development skills in praktijk te zetten."
      subject="Dashbord Design - Wordpress Theme - JAMstack Development"
    />
    <BlockImage
      :image="require('~/assets/images/steven/dashboard-design-landing-final.png')"
      :image-loading="require('~/assets/images/steven/dashboard-design-landing-final.png?lqip')"
      alt-image="inspiration for dashboard"
    />
    <BlockIntro
      author="steven"
      title="Blok 1"
      text="In dit blok ga ik de OSIRIS dashboard van de Haagse Hogeschool herontwerpen in Figma, een ontwerp programma. Ik heb nooit ontwerp gemaakt van een dashboard dus eerst heb ik in wat theorieën gedoken over het ontwerpen van dashboard. Vervolgens heb ik inspiraties gezocht op dashboard designs. Deze inspiraties gaf me een idee hoe ik de layout van de dashboard moet opstellen."
    />
    <BlockImage
      :full="false"
      :image="require('~/assets/images/steven/inspiration-dashboard.png')"
      :image-loading="require('~/assets/images/steven/inspiration-dashboard.png?lqip')"
      alt-image="inspiration for dashboard"
    />
    <BlockGallery
      author="steven"
      :images="gallery"
    />
    <BlockText
      author="steven"
      text="Na veel feedback sessies met onze docenten heb de herontwerp van de OSIRIS dashboard afgerond. Dit blok heb ik veel geleerd over het ontwerpen van dashboard en het inrichten van belangrijke data maar ook het gebruiken van verschillende kleuren. Ik ben heel trots op mijn designs en hoeveel ik heb geleerd binnen dit blok."
      link="https://www.figma.com/file/BnfsALBcUPH7ONN4hHJLyz/HHS-Osiris-Dashboard-Redesign?node-id=0%3A1/"
      linkText="zie alle schermen"
    />
    <BlockImage
      :full="false"
      :image="require('~/assets/images/steven/dashboard-design-resultaten-final.png')"
      :image-loading="require('~/assets/images/steven/dashboard-design-resultaten-final.png?lqip')"
      alt-image="OSIRIS dashboard design results page"
    />
    <BlockImage
      :full="false"
      :image="require('~/assets/images/steven/dashboard-design-resultaten-final.png')"
      :image-loading="require('~/assets/images/steven/dashboard-design-resultaten-final.png?lqip')"
      alt-image="OSIRIS dashboard design results page"
    />
    <BlockIntro
      author="steven"
      title="Blok 2"
      text="In blok 2 heb ik gekozen om richting front-end development te gaan. Tijdens mijn stage heb ik veel geleerd over Wordpress en thema maken. Daarmee wil ik verder gaan dus ik heb gekozen om een thema te maken van scratch voor onze minor website in Wordpress. Voor dit blok gebruik ik Wordpress, ACF en Timber om mijn thema te bouwen."
    />
    <BlockLogo
      author="steven"
      :logos="logos"
    />
    <BlockText
      author="steven"
      text="Voor dit blok gebruik ik Wordpress, ACF en Timber om mijn thema te bouwen. Eerst heb wat onderzoek gedaan hoe Wordpress hierarchy werkt, dit is heel belangrijk voor het bouwen van thema’s. Daarna heb ik wat schetsen gemaakt voor mijn pagina’s gebaseerd op opgezochte inspiraties. Vervolgens wat wireframes gemaakt zodat ik snel kon beginnen met de development fase. De plugins die ik voor mijn Wordpress gebruikte hielp me erg om het development proces te versnellen. ACF zorgde voor het maken van invoervelden in de achterkant van Wordpress. Hierdoor kon ik makkelijk data definiëren die ik nodig heb voor mijn eindresultaat. Met Timber kan ik makkelijker de content achterhalen voor mijn front-end. En de rest was de layout neerzetten met HTML en CSS."
      link="https://hhs-kb-86.000webhostapp.com/"
      linkText="Ga naar website"
    />
    <BlockImage
      :image="require('~/assets/images/steven/wordpress-home-page.png')"
      :image-loading="require('~/assets/images/steven/wordpress-home-page.png?lqip')"
      alt-image="Wordpress home pagina"
    />
    <BlokBlocks
      intro-text="Tijdens een masterclass van onze minor heeft een van onze docenten over JAMstack gehad, een techniek die in laatste jaren veel wordt gebruikt om website te bouwen. De prestatie van de website vergeleken met andere website is heel hoog. Dus ik wou in dit blok zelf een website maken in JAMstack."
      author="steven"
      :blok-image="require('~/assets/images/steven/netlify.png')"
      :blok-image-loading="require('~/assets/images/steven/netlify.png?lqip')"
      alt-image="netlify image"
    />
    <BlockIntro
      author="steven"
      title="Blok 3"
      text="Er zijn verschillende tools die je kan gebruiken voor het implementatie van JAMstack, ik heb gekozen om met Nuxt.js een framework van Vue en DatoCMS te gebruiken als CMS. Vroeger heb ik een paar cursussen van Vue.js gevolgd. Voor de ontwerp ik gekozen om de website van mijn vorige blok te gebruiken. Hierdoor besteed ik dus meer tijd in de technieken dan in het layout van de website."
    />
    <BlockImage
      :image="require('~/assets/images/steven/jamstack-blog-page.png')"
      :image-loading="require('~/assets/images/steven/jamstack-blog-page.png?lqip')"
      alt-image="JAMstack blog pagina"
    />
    <BlockText
      author="steven"
      text="Na een paar tutorials en het goed lezen van de documentaties kon ik de website van blok 2 herbouwen in Nuxt.js en DatoCMS. De JAMstack website vergeleken met Wordpress website van blok 2 is sneller en de implementatie van progressive image loading was makkelijk met DatoCMS.Er waren wel sommige dingen die ik niet in DatoCMS kon doen. JAMstack ga ik de toekomst zeker gebruiken en misschien een combinatie van JAMstack met Wordpress dan krijg ik beste van beide wereld."
      link="https://kb-86.netlify.app/"
      linkText="Ga naar website"
    />
    <BlockImage
      :full="false"
      :image="require('~/assets/images/steven/jamstack-blog-teaser.png')"
      :image-loading="require('~/assets/images/steven/jamstack-blog-teaser.png?lqip')"
      alt-image="JAMstack blog teaser section"
    />
    <BlockImage
      :full="false"
      :image="require('~/assets/images/steven/jamstack-single-post.png')"
      :image-loading="require('~/assets/images/steven/jamstack-single-post.png?lqip')"
      alt-image="JAMstack single post pagina"
    />
    <Footer
      author="steven"
    />
  </section>
</template>
<script>
import Header from '~/components/Header.vue';
import Profile from '~/components/Profile.vue';
import BlockIntro from '~/components/BlockIntro.vue';
import ProjectIntro from '~/components/ProjectIntro.vue';
import BlokBlocks from '~/components/BlokBlocks.vue';
import BlockText from '~/components/BlockText.vue';
import Footer from '~/components/Footer.vue';
import BlockGallery from '~/components/BlockGallery.vue';
import BlockImage from '~/components/BlockImage.vue';
import BlockLogo from '~/components/BlockLogo.vue';

export default {
  // Used for BlockGallery
  data() {
    return {
      gallery: [
        {
          src: require('~/assets/images/steven/sketch-layout.png'),
          srcLoading: require('~/assets/images/steven/sketch-layout.png?lqip'),
          alt: 'sketch of layout'
        },
        {
          src: require('~/assets/images/steven/sketch-details.png'),
          srcLoading: require('~/assets/images/steven/sketch-details.png?lqip'),
          alt: 'sketch of details page'
        },
        {
          src: require('~/assets/images/steven/sketch-catalogus.png'),
          srcLoading: require('~/assets/images/steven/sketch-catalogus.png?lqip'),
          alt: 'sketch of catalogus page'
        },
        {
          src: require('~/assets/images/steven/sketch-results.png'),
          srcLoading: require('~/assets/images/steven/sketch-results.png?lqip'),
          alt: 'sketch of results page'
        },
      ],
      logos: [
        {
          src: require('~/assets/images/steven/timber-logo.png'),
          srcLoading: require('~/assets/images/steven/timber-logo.png?lqip'),
          alt: 'Timber logo',
        },
        {
          src: require('~/assets/images/steven/wp-logo.png'),
          srcLoading: require('~/assets/images/steven/timber-logo.png?lqip'),
          alt: 'WordPress logo',
        },
        {
          src: require('~/assets/images/steven/acf-logo.png'),
          srcLoading: require('~/assets/images/steven/timber-logo.png?lqip'),
          alt: 'ACF logo',
        },
      ]
    }
  },
  components: {
    Header,
    Profile,
    ProjectIntro,
    BlokBlocks,
    BlockIntro,
    BlockText,
    Footer,
    BlockGallery,
    BlockImage,
    BlockLogo,
  },
}
</script>
<style lang="scss" scoped>
.section__personal {
  cursor: url("~assets/cursors/cursor-steven.png"), auto;

  button, a {
    &:hover {
      cursor: url("~assets/cursors/hand-steven.png"), auto;
    }
  }
}
</style>
