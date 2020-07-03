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
  'arrow-right':
    `<line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/>`,
  'home':
    `<path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path><polyline points="9 22 9 12 15 12 15 22"></polyline>`,
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
</style>