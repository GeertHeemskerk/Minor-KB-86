
<template>
  <svg
      :class="className"
      v-html="path"
      xmlns="http://www.w3.org/2000/svg" 
      width="24" 
      height="24" 
      viewBox="0 0 24 24" 
      fill="none"
      stroke="currentColor"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round">
  </svg>
</template>
<script>
const ICONS = {
  'menu-close':
    `<line x1="18" y1="6" x2="6" y2="18"></line><line x1="6" y1="6" x2="18" y2="18"></line>`,
  'menu':
    `<circle cx="7.135" cy="7.135" fill="#000" r="1.135"/><circle cx="7.135" cy="16.865" fill="#000" r="1.135"/><circle cx="16.865" cy="7.135" fill="currentColor" r="1.135"/><circle cx="16.865" cy="16.865" fill="currentColor" r="1.135"/>`,
  'chevron-left':
    `<path d="M15 18l-6-6 6-6"/>`,
  'chevron-right':
    `<path d="M9 18l6-6-6-6"/>`,
};
export default {
  props: {
    className: String,
    type: String
  },
  computed: {
    path() {
      return ICONS[this.type];
    }
  }
}
</script>
<style lang="scss" scoped>
.icons {
  &--white {
    stroke: white;
  }
}
</style>