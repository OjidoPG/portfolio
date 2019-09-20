<template>
  <v-row justify="center">
    <v-dialog v-model="bac.dialog" fullscreen hide-overlay transition="dialog-bottom-transition">
      <v-card id="card">
        <v-toolbar dark color="primary">
          <v-btn icon dark @click.stop.prevent.capture="bac.dialog = false">
            <v-icon>mdi-arrow-left-bold-circle</v-icon>
          </v-btn>
          <v-toolbar-title>Retour</v-toolbar-title>
        </v-toolbar>
        <v-row align="center" justify="center">
          <v-img id="bac" src="@/assets/BacD.jpg" max-width="600" max-height="1000"></v-img>
        </v-row>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  name: "Bac",
  props: {
    bac: {
      type: Object,
      required: true
    }
  }
};
</script>

<style>
#bac {
  transform: rotate(-90deg);
  margin: 0px;
  padding: 0px;
  margin-top: -80px;
  border: solid black 1px;
}
#card{
    background-color: rgb(82, 86, 89);
}
</style>