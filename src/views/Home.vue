<template lang="pug">
  v-container.mx-sm-12.my-6(fluid)
    .display-2.d-none.d-sm-block Welcome to Statbus!
    .display-1.d-block.d-sm-none.text-center Welcome to Statbus!
    v-divider.mr-sm-12.my-6.d-none.d-sm-block
</template>

<script>
export default {
  components: {
  },
};
</script>

<style lang="stylus" scoped>
>>> .v-divider.mr-sm-12
  @media (min-width 600px)
    margin-right 84px !important
</style>
