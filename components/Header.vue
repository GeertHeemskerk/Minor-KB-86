<template>
  <header class="header">
    <div class="header__wrapper">
      <div class="menu">
        <p class="menu__text">Menu</p>
        <Icons class-name="menu__icon icons--white" type="menu" />
      </div>
    </div>
  </header>
</template>
<script>
import Icons from '~/components/Icons.vue';

export default {
  components: {
    Icons,
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
</style>