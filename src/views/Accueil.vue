<template>
  <div>
    <v-navigation-drawer v-model="drawer" app>
      <v-list dense>
        <v-list-item>
          <v-row class="justify-center">
          <v-img
                  src="@/assets/profil.jpg"
                  max-width="150"
                  max-height="200"
                  alt="Photo de profil"
                  position="center"
          ></v-img>
          </v-row>
        </v-list-item>
        <v-list-item>
          <v-divider></v-divider>
        </v-list-item>
        <v-list-item @click="goCv">
          <v-list-item-action>
            <i class="far fa-file"></i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Curriculum vitae</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item @click="goDiplomes">
          <v-list-item-action>
            <i class="fas fa-graduation-cap"></i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Diplômes</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item @click="goXp">
          <v-list-item-action>
            <i class="far fa-folder-open"></i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Expériences</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item @click="goReal">
          <v-list-item-action>
            <i class="fas fa-keyboard"></i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Réalisations</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item @click="goCert">
          <v-list-item-action>
            <i class="fas fa-certificate"></i>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Certifications</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
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
  </div>
</template>

<script>
export default {
  name: "Accueil",
  props: {
    source: String
  },
  data: () => ({
    drawer: false
  }),
  methods: {
    goCv() {
      alert("goCv");
    },
    goDiplomes() {
      alert("goDiplomes");
    },
    goXp() {
      alert("goXp");
    },
    goReal() {
      alert("goReal");
    },
    goCert() {
      alert("goCert");
    }
  }
};
</script>