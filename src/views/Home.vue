<template lang="pug">
  v-container.mx-sm-12(fill-height)
    v-layout(column)
      div
        .display-2.d-none.d-sm-block Welcome to Statbus!
        .display-1.d-block.d-sm-none.text-center Welcome to Statbus!
        v-divider.my-6.d-none.d-sm-block

      div(class='d-flex flex-wrap align-center \
        justify-space-around mx-sm-n6 mx-xs-3 \
        mt-xs-6 mx-md-auto my-md-auto'
      )
        v-card.mb-6.mx-3(
          v-for="n in 4"
          :key="n"
          hover
        )
          v-container.px-6.py-10
            .headline.font-weight-light Test
            .display-2.font-weight-light 123
            .headline.font-weight-light Total somethings
</template>

<script>
export default {
  components: {
  },
};
</script>

<style lang="stylus" scoped>
// Breakpoints broken somehow WHY
>>> .d-flex.mt-xs-6
  @media (max-width 599px)
    margin-top 24px !important
>>> .d-flex.mx-xs-3
  @media (max-width 599px)
    margin-left 12px !important
    margin-right 12px !important
>>> .v-card
  @media (max-width 599px)
    min-width 100%
// You can go right to hell demon query
.container.fill-height
  @media (min-width 960px)
    max-width unset
</style>
