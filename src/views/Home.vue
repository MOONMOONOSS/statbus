<template lang="pug">
  v-container.mx-sm-12(fill-height)
    v-layout(column)
      div
        .display-2.d-none.d-sm-block Welcome to Statbus!
        .display-1.d-block.d-sm-none.text-center Welcome to Statbus!
        v-divider.my-6.d-none.d-sm-block

      div(class='d-flex flex-wrap align-center \
        mx-sm-n6 mx-xs-3 mt-xs-6 my-md-auto'
      )
        //- TODO: Make lg+ conditional layout
        DashCard(
          v-for="(card, i) in cards"
          :key="i"
          :card="card"
        )
</template>

<script>
import DashCard from '../components/home/DashCard.vue';

export default {
  components: {
    DashCard,
  },
  data: () => ({
    cards: [
      {
        heading: 'Cataloging',
        number: '1,003',
        subText: 'Total deaths',
      },
      {
        heading: 'With data from',
        number: '162',
        subText: 'Total rounds',
      },
      {
        heading: 'Gathered by over',
        number: '101,700',
        subText: 'Minutes of gameplay',
      },
      {
        heading: 'Check out',
        number: '10',
        subText: 'Books in our library',
      },
    ],
  }),
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
// You can go right to hell demon query
.container.fill-height
  @media (min-width 960px)
    max-width unset
</style>
