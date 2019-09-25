<template lang="pug">
  v-app-bar(
    color="primary"
    app
    dark
  )
    v-app-bar-nav-icon.d-flex.d-sm-none
    v-toolbar-title {{ appName }}
    v-spacer
    v-tooltip(
      v-for="(data) in buttons"
      :key="data.icon"
      bottom
    )
      template(v-slot:activator="{ on }")
        v-btn.d-none.d-sm-flex.space-out(
          v-on="$vuetify.breakpoint.mdAndUp ? null : on"
          :icon="!$vuetify.breakpoint.mdAndUp"
          :text="$vuetify.breakpoint.mdAndUp"
        )
          v-icon(:left="$vuetify.breakpoint.mdAndUp") {{ data.icon }}
          | {{ $vuetify.breakpoint.mdAndUp ? data.text : '' }}
      span {{ data.text }}
    v-tooltip(
      v-for="(data) in sidecons"
      :key="data.icon"
      bottom
    )
      template(v-slot:activator="{ on }")
        v-btn(
          v-on="on"
          icon
        ): v-icon {{ data.icon }}
      span {{ data.text }}
</template>

<script>
export default {
  name: 'ApplicationBar',
  computed: {
    appName: () => process.env.VUE_APP_NAME,
  },
  data: () => ({
    buttons: [
      {
        icon: 'fa-chart-pie',
        text: 'Rounds',
      },
      {
        icon: 'fa-skull',
        text: 'Deaths',
      },
      {
        icon: 'fa-book',
        text: 'Library',
      },
      {
        icon: 'fa-poll-h',
        text: 'Polls',
      },
      {
        icon: 'fa-globe',
        text: 'Extras',
      },
    ],
    sidecons: [
      {
        icon: 'fa-search',
        text: 'Search',
      },
      {
        icon: 'fa-user-circle',
        text: 'Account',
      },
    ],
  }),
};
</script>

<style lang="stylus" scoped>
>>> .v-btn--text, .v-btn--icon
  transition-duration .5s
  transition-property all
  transition-timing-function cubic-bezier(.25, .8, .5, 1)
>>> .v-btn--icon.space-out
  transition-duration 1s
  min-width 60px
>>> .v-toolbar__title
  // Makes our title not selectable
  // Just personal preference
  user-select none
</style>
