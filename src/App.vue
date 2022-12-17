<template>
  <!-- unplugin-vue-components auto import -->
  <v-app>
    <Header />
    <v-main>
      <v-badge>
        <v-icon icon="mdi-vuetify" size="x-large"></v-icon>
      </v-badge>
      <v-container class="px-0" fluid>
        <v-switch
          v-model="switch1"
          :label="`DynamicMovement: ${switch1.toString()}`"
        ></v-switch>
      </v-container>
      <Form />
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      switch1: true,
    };
  },
};
</script>

<style scoped>
.v-main {
  padding: 1rem 0;
}
</style>
