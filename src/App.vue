<template lang="pug">
  v-app
    AppBar

    v-content: router-view
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
