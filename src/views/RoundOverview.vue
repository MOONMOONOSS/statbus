<template lang="pug">
  v-container.mx-sm-12(fill-height)
    v-layout(column)
      v-col.shrink
        .display-2.d-none.d-sm-block Round Listings
        .display-1.d-block.d-sm-none.text-center Round Listings
        v-divider.my-6.d-none.d-sm-block
      v-spacer
      v-col.text-center.shrink
        v-pagination(
          v-model="page"
          :length="15"
          :total-visible="7"
        )
</template>

<script>
export default {
  data: () => ({
    page: 1,
  }),
};
</script>
