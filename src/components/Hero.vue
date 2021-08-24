<template>
  <div class="hero" :style="cssVars">
    😀
  </div>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    x: Number,
    y: Number
  },
  computed: {
    cssVars() {
      return {
        '--x': this.x,
        '--y': this.y
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hero {
  grid-column: var(--x);
  grid-row: var(--y);
}
</style>
