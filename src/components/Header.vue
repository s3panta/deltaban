<template>
    <div class="top_bar">
<!-- //////////////////////////////HambergurBtn&Avatar//////////////////////////////// -->
        <v-container class="fill-height">
            <v-row align="center" justify="space-between">
                <v-btn icon color="teal darken-4" @click.stop="drawer = !drawer">
                    <v-icon>mdi-format-align-left</v-icon>
                </v-btn>
                <v-avatar id="avatar">
                    <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
                </v-avatar>

            </v-row>
        </v-container>
<!-- //////////////////////////////Drawer//////////////////////////////// -->
        <v-navigation-drawer v-model="drawer" absolute temporary>
            <v-list-item>
                <v-list-item-avatar>
                    <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                    <v-list-item-title>John Leider</v-list-item-title>
                </v-list-item-content>
            </v-list-item>

            <v-divider></v-divider>

            <v-list dense>
                <v-list-item v-for="item in items" :key="item.title" link>
                    <v-list-item-icon>
                        <v-icon>{{ item.icon }}</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </div>
</template>

<script>
    export default {
        name: 'App',

        components: {

        },

        data: () => ({

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
        watch: {
            group() {
                this.drawer = false
            },
        },
    }
</script>

<style scoped>
    .top_bar {
        padding-top: 26px;
        padding-left: 30px;
        padding-right: 30px;
        background-color: #EEEEEE;
    }

    #avatar {
        border-radius: 10%;
    }
</style>