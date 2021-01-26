<template>
    <v-bottom-navigation v-model="value" background-color="#FFFFFF" dark shift class="BottomNav">
        <v-btn>
            <v-icon color="teal darken-4">mdi-home</v-icon>
        </v-btn>

        <v-btn>
            <v-icon color="grey darken-1">mdi-message-text</v-icon>
        </v-btn>

        <v-btn>
            <v-icon color="grey darken-1">mdi-plus</v-icon>
        </v-btn>

        <v-btn>
            <v-icon color="grey darken-1">mdi-cards-heart</v-icon>
        </v-btn>

        <v-btn>
            <v-icon color="grey darken-1">mdi-account</v-icon>
        </v-btn>
    </v-bottom-navigation>
</template>

<script>
    export default {
        data: () => ({
            value: 1,
            drawer: false,
            group: null,
            items: [{
                    title: 'Dashboard',
                    icon: 'mdi-view-dashboard'
                },
                {
                    title: 'Photos',
                    icon: 'mdi-image'
                },
                {
                    title: 'About',
                    icon: 'mdi-help-box'
                },
            ],
            right: null,
        }),
        computed: {

        },
    }
</script>

<style scoped>
    .BottomNav {
        position: fixed;
        bottom: 0;
        left: 0;
        width: 100%;
    }
</style>