<template lang="pug">
  v-card.mb-6.mx-3.flex-grow-1(hover)
    v-container.px-6.py-10
      .headline.font-weight-light {{ card.heading }}
      .display-2.font-weight-light {{ card.number }}
      .headline.font-weight-light {{ card.subText }}
</template>

<script>
export default {
  props: ['card'],
};
</script>

<style lang="stylus" scoped>
>>> .v-card
  @media (max-width 599px)
    min-width 100%
</style>
