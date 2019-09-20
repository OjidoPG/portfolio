<template>
  <div>
    <v-treeview rounded dense hoverable :items="items">
      <template slot="label" slot-scope="{ item }">
        <v-icon>{{item.icon}}</v-icon>
        <a @click="openDialog(item)">{{ item.name }}</a>
      </template>
    </v-treeview>
  </div>
</template>

<script>
export default {
  props: ["cv", "bac", "dev", "inf", "sec"],
  methods: {
    openDialog(item) {
      switch (item.id) {
        case 1:
          this.cv.dialog = true;
          break;
        case 3:
          this.bac.dialog = true;
          break;
        case 4:
          this.dev.dialog = true;
          break;
        case 5:
          this.inf.dialog = true;
          break;
          case 6:
              this.sec.dialog=true;
              break;
        default:
          break;
      }
    }
  },
  data: () => ({
    items: [
      {
        id: 1,
        name: "Curriculum vitae",
        icon: "mdi-file-account"
      },
      {
        id: 2,
        name: "Diplômes",
        icon: "mdi-school",
        children: [
          {
            id: 3,
            name: "Baccalauréat"
          },
          {
            id: 4,
            name: "Développeur"
          },
          {
            id: 5,
            name: "Infirmier"
          },
          {
            id: 6,
            name: "Secouriste"
          }
        ]
      },
      {
        id: 7,
        name: "Expériences",
        icon: "mdi-file-export",
        children: [
          {
            id: 8,
            name: "Développeur"
          },
          {
            id: 9,
            name: "Infirmier"            
          },
          {
            id: 10,
            name: "Autres"
          }
        ]
      },
      {
        id: 11,
        name: "Réalisations",
        icon: "mdi-checkbox-marked"
      },
      {
        id: 12,
        name: "Certifications",
        icon: "mdi-file-certificate",
        children:[
            {
                id:13,
                name:"C#"
            },
            {
                id:14,
                name:"PHP - MySQL"
            },
            {
                id:15,
                name:"Sécurité numérique"
            }
        ]
      }
    ]
  })
};
</script>