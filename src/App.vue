<template>
<!-- Aufgabe 2 --Anordnung spielt keine rolle -->
  <div id="app">
    <v-data-table
      :headers="headers"
      :items="desserts"
      item-key="name"
      class="elevation-1"
      :search="search"
      :custom-filter="filterOnlyCapsText"
    >
      
      <template v-slot:body.append>
        <tr>
          <td></td>
          <td>
            <v-text-field v-model="calories" type="number" label="Less">
            </v-text-field>
          </td>
          <td colspan="4"></td>
        </tr>
      </template>
      <template v-slot:top>
        <v-text-field
          v-model="search"
          label="Search"
          class="mx-4"
        ></v-text-field>
      </template>
    </v-data-table>
  </div>
</template>

<script>
// import AppButton from '@/components/AppButton.vue';
// // import Sheet from '@/components/Sheet.vue';
// import AppLayout from '@/components/AppLayout.vue';

export default {
  name: 'App',
  components: {
    // AppButton,
    // // Sheet,
    // AppLayout,
  },
  data: () => ({
    //
  }),
};
</script>
