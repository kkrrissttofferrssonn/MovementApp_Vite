<template>
  <!-- unplugin-vue-components auto import -->
  <v-app>
    <Header />
    <v-main>
      <v-card>
        <v-layout>
          <v-navigation-drawer theme="dark">
            <v-list nav>
              <v-list-item
                prepend-icon="mdi-email"
                title="Inbox"
                value="inbox"
              ></v-list-item>
              <v-list-item
                prepend-icon="mdi-account-supervisor-circle"
                title="Supervisors"
                value="supervisors"
              ></v-list-item>
              <v-list-item
                prepend-icon="mdi-clock-start"
                title="Clock-in"
                value="clockin"
              ></v-list-item>

              <v-list-item title="ArmSwing" value="armswing"></v-list-item>
              <v-list-item title="LegSwing" value="legswing"></v-list-item>
              <v-list-item title="BodySwing" value="bodyswing"></v-list-item>
              <v-list-item title="TwistSwing" value="TwistSwing"></v-list-item>
              <v-list-item title="WhipSwing" value="WhipSwing"></v-list-item>
              <v-list-item title=""></v-list-item>
              <v-list-item title=""></v-list-item>
              <v-list-item title=""></v-list-item>
              <v-list-item title=""></v-list-item>
              <v-list-item title=""></v-list-item>
            </v-list>
          </v-navigation-drawer>
          <v-main style="height: 250px"></v-main>
        </v-layout>
      </v-card>
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
  background: Green;
}
</style>
