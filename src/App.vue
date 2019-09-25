<template lang="pug">
  v-app
    AppBar

    v-content: v-container(fluid, fill-height): router-view
</template>

<script>
import AppBar from './components/common/AppBar.vue';

export default {
  name: 'App',
  components: {
    AppBar,
  },
  data: () => ({
    //
  }),
};
</script>

<style lang="stylus">
html
  overflow-y auto !important
// You can go right to hell demon query
.container
  @media (min-width 960px)
    max-width unset
</style>
