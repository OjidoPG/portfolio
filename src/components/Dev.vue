<template>
  <v-row justify="center">
    <v-dialog v-model="dev.dialog" fullscreen hide-overlay transition="dialog-bottom-transition">
      <v-card id="card">
        <v-toolbar dark color="primary">
          <v-btn icon dark @click.stop.prevent.capture="dev.dialog = false">
            <v-icon>mdi-arrow-left-bold-circle</v-icon>
          </v-btn>
          <v-toolbar-title>Retour</v-toolbar-title>
        </v-toolbar>
        <v-row align="center" justify="center">
          <v-img id="dev" src="@/assets/CDI.jpg" max-width="600" max-height="1000"></v-img>
        </v-row>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  name: "dev",
  props: {
    dev: {
      type: Object,
      required: true
    }
  }
};
</script>

<style>
#dev {
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