<template>
    <v-row justify="center">
        <v-dialog v-model="cv.dialog" fullscreen hide-overlay transition="dialog-bottom-transition">
            <v-card>
                <v-toolbar dark color="primary">
                    <v-btn icon dark @click.stop.prevent.capture="cv.dialog = false">
                        <v-icon>mdi-close</v-icon>
                    </v-btn>
                    <v-toolbar-title>Settings</v-toolbar-title>
                    <div class="flex-grow-1"></div>
                </v-toolbar>
                <v-img
                src="@/assets/ocr.jpg"
                max-width="150"
                max-height="200"
                alt="Photo de profil"
                position="center"
        ></v-img>
            </v-card>
        </v-dialog>
    </v-row>
</template>

<script>
    export default {
        name: 'Cv',
        data () {
            return {
                notifications: false,
                sound: true,
                widgets: false,
            }
        },
        props:{
            cv:{
                type:Object,
                required:true
            }
        }
    }
</script>