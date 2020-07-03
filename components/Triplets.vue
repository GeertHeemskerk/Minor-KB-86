<template>
  <div>
    <div v-lazy-container="{ selector: 'img' }" class="section__wrapper">
      <img 
        :data-src="left" 
        :data-loading="leftLoading" 
        :alt="leftAlt" 
      />
      <img 
        :data-src="middle" 
        :data-loading="middleLoading" 
        :alt="middleAlt" 
      />
      <img 
        :data-src="right" 
        :data-loading="rightLoading" 
        :alt="rightAlt" 
      />
    </div>
  </div>
</template>
<script>
export default {
  props: {
    left: String,
    leftLoading: String,
    leftAlt: String,
    middle: String,
    middleLoading: String,
    middleAlt: String,
    right: String,
    rightLoading: String,
    rightAlt: String,
  },
}
</script>
<style lang="scss" scoped>
.section__wrapper {
  width: 100%;
  padding: 1.5rem 3rem;
}

img {
  display: block;
  width: 100%;
  height: auto;
  position: relative;
  margin-bottom: 3rem;
}

@media(min-width: $mq-tablet) {
  .section__wrapper {
    display: flex;
    padding: 3rem 0 8rem 0;
  }

  img {
    width: 30%;
    margin-bottom: 0;
  }

  img:nth-child(2) {
    margin: 0 5%;
    top: 3rem;
  }
}

@media(min-width: $mq-s-laptop) {
  img:nth-child(2) {
    top: 4rem;
  }
}

@media(min-width: $mq-xl-laptop) {
  img:nth-child(2) {
    top: 5rem;
  }
}

@media(min-width: $mq-desktop) {
  img:nth-child(2) {
    top: 6rem;
  }

  .section {
    &__wrapper {
      padding-bottom: 11rem;
    }
  }
}
</style>
