<template>
    <div>
        <v-treeview
                rounded
                dense
                hoverable
                :items="items"
        >
            <template slot="label" slot-scope="{ item }">
                <i :class=item.icon>&nbsp;&nbsp;&nbsp;</i>
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
                    icon: 'far fa-file'
                },
                {
                    id: 2,
                    name: 'Diplômes :',
                    icon: 'fas fa-graduation-cap',
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
                    name: 'Expériences :',
                    icon: 'far fa-folder-open',
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
                    icon: 'fas fa-keyboard'
                },
                {
                    id: 12,
                    name: 'Certifications',
                    icon: 'fas fa-certificate'
                },
            ],
        }),
    }
</script>