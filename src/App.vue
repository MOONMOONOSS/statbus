<template lang="pug">
  v-app
    v-app-bar(app)
      v-toolbar-title.headline.text-uppercase
        span Vuetify
        span.font-weight-light MATERIAL DESIGN
      v-spacer
      v-btn(
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      )
        span.mr-2 Latest Release
        v-icon fas fa-external-link-alt

    v-content: router-view
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    //
  }),
};
</script>
