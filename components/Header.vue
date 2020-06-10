<template>
  <header class="header">
    <div class="header__wrapper">
        <transition name="slide-fade">
          <button class="menu__button button--clean" v-if="!open" key="on" @click="open = true">
            <div class="menu">
              <p class="menu__text">Menu</p>
              <Icons class-name="menu__icon icons--white" type="menu" />
            </div>
          </button>
          <button class="menu__button button--clean" v-else key="off" @click="open = false">
            <div class="menu">
              <p class="menu__text">Close Menu</p>
              <Icons class-name="menu__icon icons--white" type="menu-close" />
            </div>
          </button>
        </transition>
      </div>
  </header>
</template>
<script>
import Icons from '~/components/Icons.vue';

export default {
  data() {
    return {
      open: false
    }
  },
  components: {
    Icons,
  },
  methods: {
  }
}
</script>
<style lang="scss" scoped>
.header {
  height: 85px;
  width: 100%;

  &__wrapper {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    width: 90%;
    margin: 0 auto;
    height: 100%;
  }
}

.menu {
  display: flex;
  align-items: center;

  &__button {
    cursor: pointer;
  }

  &__text {
    font-family: $f-heading;
    color: white;
    font-size: 0.625rem;
    letter-spacing: 1px;
    padding-right: 1rem;
  }

  &__icon {
    width: 14px;
    height: 14px;
  }
}

.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all .6s;
}
.slide-fade-enter,
.slide-fade-leave-active {
  opacity: 0;
}
.slide-fade-enter {
  transform: translateX(31px);
}
.slide-fade-leave-active {
  transform: translateX(-31px);
}
</style>