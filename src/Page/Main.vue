<template>
    <div class="main_container">
<!-- //////////////////////////////top-text&textField//////////////////////////////// -->
        <div class="Top_Text">
            <h2>Where would you like <br> to go ?</h2>
        </div>
        <v-col cols="12" sm="6">
            <v-text-field v-model="last" label="Search" solo-inverted append-icon="mdi-magnify">
            </v-text-field>
        </v-col>
<!-- //////////////////////////////Category//////////////////////////////// -->
        <div class="Category">
            <div class="Title">
                <h3>Category</h3>
            </div>
            <div class="Category_Cards">
                <div class="Category_Cards_Box">
                    <div class="logo_Card bluecolor">
                        <v-btn icon color="grey lighten-5">
                            <v-icon>mdi-map-legend</v-icon>
                        </v-btn>
                    </div>
                    <p style="color:#004D40;">Places</p>
                </div>
                <div class="Category_Cards_Box">
                    <div class="logo_Card">
                        <v-btn icon color="grey darken-3">
                            <v-icon>mdi-airplane-takeoff</v-icon>
                        </v-btn>
                    </div>
                    <p>Flight</p>
                </div>
                <div class="Category_Cards_Box">
                    <div class="logo_Card">
                        <v-btn icon color="grey darken-3">
                            <v-icon>mdi-city-variant-outline</v-icon>
                        </v-btn>
                    </div>
                    <p>Hotels</p>
                </div>
                <div class="Category_Cards_Box">
                    <div class="logo_Card">
                        <v-btn icon color="grey darken-3">
                            <v-icon>mdi-bowl-mix</v-icon>
                        </v-btn>
                    </div>
                    <p>Foods</p>
                </div>

            </div>
        </div>
<!-- //////////////////////////////SlickSlider//////////////////////////////// -->
        <Slick />

    </div>
</template>

<script>
    import Slick from "../components/Slider/Slick"
    export default {
        components: {
            Slick
        },
    }
</script>

<style scoped>
    .main_container {
        width: 100%;
        height: 100%;
        background-color: #EEEEEE;

    }

    .Top_Text {
        margin-top: 20px;
        margin-left: 20px;
        margin-right: 20px;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        color: #004D40;
    }

    .Title {
        color: #004D40;
    }

    .Category {

        margin-left: 20px;
        margin-right: 20px;
    }

    .Category_Cards {
        width: 100%;

        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;

    }

    .Category_Cards_Box {
        width: 65px;


        margin-top: 20px;

        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
    }

    .logo_Card {
        width: 65px;
        height: 65px;
        background-color: #BDBDBD;
        border-radius: 10px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-bottom: 10px;
    }

    .bluecolor {
        background-color: #004D40 !important;
    }
</style>