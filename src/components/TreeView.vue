<template>
    <div>
        <v-treeview
                rounded
                dense
                hoverable
                :items="items"
        >
            <template slot="label" slot-scope="{ item }">
               <v-icon>{{item.icon}}</v-icon>
                <a @click="openDialog(item)">{{ item.name }}</a>
            </template>
        </v-treeview>
    </div>
</template>

<script>
    export default {
        props: ['cv'],
        methods: {
            openDialog(item) {
                switch (item.id) {
                    case 1 :
                        this.cv.dialog = true;
                        break;
                    case 3:
                        alert('Baccalauréat');
                        break;
                }
            }
        },
        data: () => ({
            items: [
                {
                    id: 1,
                    name: 'Curriculum vitae',
                    icon: 'mdi-file-account'
                },
                {
                    id: 2,
                    name: 'Diplômes',
                    icon: 'mdi-school',
                    children: [
                        {
                            id: 3,
                            name: 'Baccalauréat'
                        },
                        {
                            id: 4,
                            name: 'Développeur'
                        },
                        {
                            id: 5,
                            name: 'Infirmier'
                        },
                        {
                            id: 6,
                            name: 'Secouriste'
                        }
                    ],
                },
                {
                    id: 7,
                    name: 'Expériences',
                    icon: 'mdi-file-export',
                    children: [
                        {
                            id: 8,
                            name: 'Infirmier'
                        },
                        {
                            id: 9,
                            name: 'Développeur'
                        },
                        {
                            id: 10,
                            name: 'Autres'
                        }
                    ],
                },
                {
                    id: 11,
                    name: 'Réalisations',
                    icon: 'mdi-checkbox-marked'
                },
                {
                    id: 12,
                    name: 'Certifications',
                    icon: 'mdi-file-certificate'
                },
            ],
        }),
    }
</script>