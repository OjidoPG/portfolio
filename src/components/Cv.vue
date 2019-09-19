<template>
  <v-row justify="center">
    <v-dialog v-model="cv.dialog" fullscreen hide-overlay transition="dialog-bottom-transition">
      <v-toolbar dark color="primary">
        <v-btn icon dark @click.stop.prevent.capture="cv.dialog = false">
          <v-icon>mdi-arrow-left-bold-circle</v-icon>
        </v-btn>
        <v-toolbar-title>Retour</v-toolbar-title>
      </v-toolbar>
      <object data="/CV.pdf" type="application/pdf"></object>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  name: "Cv",
  props: {
    cv: {
      type: Object,
      required: true
    }
  }
};
</script>

<style>
object {
  height: 90%;
  width: 90%;
  margin: 0px;
  padding: 0px;
}
</style>