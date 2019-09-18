<template>
  <div>
    <v-navigation-drawer v-model="drawer" app>
      <v-row class="justify-center mt-5 mb-5">
        <v-img
                src="@/assets/profil.jpg"
                max-width="150"
                max-height="200"
                alt="Photo de profil"
                position="center"
        ></v-img>
      </v-row>
      <v-divider></v-divider>
      <tree-view :cv="cv"></tree-view>
    </v-navigation-drawer>

    <v-app-bar app color="indigo" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Menu</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <v-container class="fill-height">
        <v-row align="center" justify="center">
        </v-row>

      </v-container>
    </v-content>
    <v-footer color="indigo" app>
      <span class="white--text">&copy; 2019 - GIRAUD Pascal</span>
    </v-footer>

      <cv :cv="cv"></cv>
  </div>
</template>

<script>
  import TreeView from '../components/TreeView';
  import Cv from '../components/Cv';

export default {
  name: "Accueil",
  components:{
    TreeView,
      Cv
  },
  props: {
    source: String
  },
  data: () => ({
    drawer: false,
      cv: {
          dialog: false
      }
  })
};
</script>