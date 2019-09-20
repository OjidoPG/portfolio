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
      <tree-view :cv="cv" :bac="bac" :dev="dev" :inf="inf" :sec="sec"></tree-view>
    </v-navigation-drawer>

    <v-app-bar app color="indigo" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Menu</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <div>
        <p class="lead mb-5">
          Pendant plus de dix ans, j’ai mis à profit mon expérience dans les relations humaines, dans la compréhension de l’autre et dans la résolution de situations critiques pour venir en aide à mes patients.
          <br />Ah oui, j'ai oublié de vous dire, j'ai été infirmier !
          <br />Cependant, quoique passionnant, ce métier ne permettait pas de mettre a profit ma créativité et ne permettait pas d’observer les résultats des actions menées.
          <br />J’ai donc décidé de me réorienter pour me diriger vers une autre passion, l’informatique.
          <br />Après une période de réorientation, j’ai obtenu le titre de "Concepteur Développeur Informatique" à l’AFPA en juin 2017. J’ai travaillé un an comme développeur informatique C# ASP.Net MVC 5 (razor).
          <br />J’ai ensuite décidé de poursuivre ma montée en compétence en rejoignant le CESI pour une POEC RIL.
          <br />J’ai depuis trouvé un emploi au sein de la société C2i santé.
        </p>
      </div>
      
    </v-content>
    <v-footer color="indigo" app>
      <span class="white--text">&copy; 2019 - GIRAUD Pascal</span>
      <a href="https://www.linkedin.com/in/pascal-giraud-1a2513128" target="_blank">
         <v-icon>mdi-linkedin-box</v-icon>
        </a>
        <a href="https://github.com/OjidoPG" target="_blank">
          <v-icon>mdi-github-circle</v-icon>
        </a>
        <a href="https://www.facebook.com/pascal.giraud.1485537" target="_blank">
          <v-icon>>mdi-facebook-box</v-icon>
        </a>
    </v-footer>
    <cv :cv="cv"></cv>
    <bac :bac="bac"></bac>
    <dev :dev="dev"></dev>
    <inf :inf="inf"></inf>
    <sec :sec="sec"></sec>
  </div>
</template>

<script>
import TreeView from "../components/TreeView";
import Cv from "../components/Cv";
import Bac from "../components/Bac";
import Dev from "../components/Dev";
import Inf from "../components/Inf";
import Sec from "../components/Sec";

export default {
  name: "Accueil",
  components: {
    TreeView,
    Cv,
    Bac,
    Dev,
    Inf,
    Sec
  },
  data: () => ({
    drawer: false,
    cv: {
      dialog: false
    },
    bac: {
      dialog: false
    },
    dev: {
      dialog: false
    },
    inf: {
      dialog: false
    },
    sec: {
      dialog: false
    }
  })
};
</script>