<template>
    <div class="main_container">
        <div class="Top_Text">
            <h2>Where would you like <br> to go ?</h2>
        </div>
        <v-col cols="12" sm="6">
            <v-text-field v-model="last" label="Last Name" solo-inverted append-icon="mdi-magnify">
            </v-text-field>
        </v-col>
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


        <div class="cards">
            <div class="slider">
                <VueSlickCarousel v-bind="settings">
                    <div>
                        <div class="img_box">
                            <img src="../assets/maldive.jpg" alt="...">
                            <div class="img_title">
                                <p>Maldive</p>
                            </div>
                        </div>

                    </div>
                    <div>
                        <div class="img_box">
                            <img src="../assets/istanbul.jpg" alt="...">
                            <div class="img_title">
                                <p>Italy</p>
                            </div>
                        </div>
                    </div>
                    <div>
                        <div class="img_box">
                            <img src="../assets/italy.jpg" alt="...">
                            <div class="img_title">
                                <p>Canada</p>
                            </div>
                        </div>
                    </div>

                </VueSlickCarousel>

            </div>
        </div>
    </div>
</template>

<script>
    import VueSlickCarousel from 'vue-slick-carousel'
    import 'vue-slick-carousel/dist/vue-slick-carousel.css'
    // optional style for arrows & dots
    import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
    export default {
        components: {
            VueSlickCarousel
        },

        data() {
            return {
                settings: {
                    "dots": false,
                    "arrows": false,
                    "focusOnSelect": true,
                    "infinite": true,
                    "speed": 500,
                    "slidesToShow": 2,
                    "slidesToScroll": 3,
                    "touchThreshold": 5,
                    
                    "centerPadding": "20px",
                    "swipeToSlide": true,
                    "rtl": false,
                    "autoplay": false,
                    "responsive": [{
                            "breakpoint": 1024,
                            "settings": {
                                "slidesToShow": 2,
                                "slidesToScroll": 3,
                                "infinite": true,
                                "dots": true
                            }
                        },
                        {
                            "breakpoint": 600,
                            "settings": {
                                "slidesToShow": 2,
                                "slidesToScroll": 2,
                                "initialSlide": 2
                            }
                        },
                        {
                            "breakpoint": 480,
                            "settings": {
                                "slidesToShow": 2,

                            }
                        }
                    ]

                },
            }
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
.Title{
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

    .cards {
        margin-top: 30px;
        margin-bottom: 60px;
        margin-left: 10px;
    }

    .img_box {
        position: relative;


    }

    .img_box>img {
        width: 200px;
        height: 250px;
        border-radius: 20px;
    }

    .img_title {
        position: absolute;
        top: 10px;
        left: 5px;
        color: #EEEEEE;
    }
                @media only screen and (max-width: 1940px) {
        .img_box>img {
            width: 450px;
        height: 500px;

        }
    }
            @media only screen and (max-width: 1024px) {
        .img_box>img {
            width: 350px;
        height: 400px;

        }
    }
        @media only screen and (max-width: 600px) {
        .img_box>img {
            width: 200px;
        height: 250px;

        }
    }

    @media only screen and (max-width: 400px) {
        .img_box>img {
            width: 170px;
            height: 200px;

        }
    }
        @media only screen and (max-width: 320px) {
        .img_box>img {
            width: 150px;
            height: 200px;

        }
    }
</style>