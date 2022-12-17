<script setup lang="ts">
// unplugin-auto-import will declare it on src/auto-imports.d.ts
const name = ref('');
const disabled = computed(() => {
  return name.value && name.value.trim().lenght > 0;
});
const sayHi = () => {
  name.value && alert(`Hi ${name.value}`);
};
</script>

<template>
  <section>
    <header>
      <h2>Add MovementName</h2>
    </header>
    <form @submit.prevent="sayHi">
      <v-form>
        <v-container>
          <v-row>
            <v-col cols="12" sm="6" md="3">
              <v-text-field label="Regular"></v-text-field>
            </v-col>

            <v-col cols="12" sm="6" md="3">
              <v-text-field
                label="Regular"
                placeholder="Placeholder"
              ></v-text-field>
            </v-col>

            <v-col cols="12" sm="6" md="3">
              <v-text-field label="Solo" solo></v-text-field>
            </v-col>

            <v-col cols="12" sm="6" md="3">
              <v-text-field
                label="Solo"
                placeholder="Placeholder"
                solo
              ></v-text-field>
            </v-col>

            <v-col cols="12" sm="6" md="3">
              <v-text-field label="Filled" filled></v-text-field>
            </v-col>

            <v-col cols="12" sm="6" md="3">
              <v-text-field
                label="Filled"
                placeholder="Placeholder"
                filled
              ></v-text-field>
            </v-col>

            <v-col cols="12" sm="6" md="3">
              <v-text-field label="Outlined" outlined></v-text-field>
            </v-col>

            <v-col cols="12" sm="6" md="3">
              <v-text-field
                label="Outlined"
                placeholder="Placeholder"
                outlined
              ></v-text-field>
            </v-col>
          </v-row>
        </v-container>
      </v-form>
      <v-text-field
        autofocus
        label="Add your movement name here?"
        v-model="name"
      ></v-text-field>
      <v-btn
        type="submit"
        :disabled="disabled"
        variant="outlined"
        color="primary"
        text
      >
        Say hello
      </v-btn>
    </form>
  </section>
</template>

<style scoped>
section {
  padding: 1rem 1.5rem;
}
</style>
