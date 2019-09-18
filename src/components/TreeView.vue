<template>
    <v-treeview
            rounded
            dense
            hoverable
            :items="items"
    >
        <template slot="label" slot-scope="{ item }">
            <i v-bind:class="{string:item.icon}">&nbsp;&nbsp;&nbsp;</i>
            <a @click="openDialog(item)">{{ item.name }}</a>
        </template>
    </v-treeview>
</template>

<script>
    export default {
        methods:{
            openDialog(item){
                alert(item.id);
            }
        },
        data: () => ({
            items: [
                {
                    id: 1,
                    name: 'Curriculum vitae',
                    icon:'far fa-file',
                    children:null
                },
                {
                    id: 2,
                    name: 'Diplômes :',
                    children: [
                        {
                            id: 3,
                            name: 'Baccalauréat'
                        },
                        {
                            id:4,
                            name:'Développeur'
                        },
                        {
                            id:5,
                            name:'Infirmier'
                        },
                        {
                            id:6,
                            name:'Secouriste'
                        }
                    ],
                },
            ],
        }),
    }
</script>