<template lang="pug">
  v-container(fill-height)
    v-layout(column)
      v-col.text-center.shrink
        v-data-table.elevation-1(
          dense
          :headers="headers"
          :items="rounds"
          :items-per-page="25"
          :search="search"
          item-key="id"
        )
          template(v-slot:top)
            v-toolbar(
              flat
              color="white"
            )
              v-toolbar-title Round Listings
              v-divider.mx-4(
                inset
                vertical
              )
              v-spacer
              v-toolbar-items.d-none.d-sm-flex
                v-text-field(
                  clearable
                  flat
                  solo
                  v-model="search"
                  prepend-icon="fa-search"
                  label="Search"
                )
            v-text-field.d-flex.d-sm-none.mx-4(
              clearable
              flat
              solo
              v-model="search"
              prepend-icon="fa-search"
              label="Search"
              style="max-height: 48px"
            )
</template>

<script>
export default {
  data: () => ({
    headers: [
      {
        text: 'ID',
        value: 'id',
      },
      {
        text: 'Mode',
        value: 'mode',
      },
      {
        text: 'Result',
        value: 'result',
      },
      {
        text: 'Map',
        value: 'map',
      },
      {
        text: 'Start',
        value: 'startTime',
      },
      {
        text: 'Duration',
        value: 'duration',
      },
      {
        text: 'End',
        value: 'endTime',
      },
      {
        text: 'Server',
        value: 'server',
      },
    ],
    rounds: [
      {
        id: 162,
        mode: 'Traitor',
        result: 'Proper Completion',
        map: 'PubbyStation',
        startTime: '2019-09-25 04:21:24',
        duration: '08:53:40',
        endTime: '2019-09-25 13:10:52',
        server: 'MoonStation',
      },
    ],
    search: '',
  }),
};
</script>
