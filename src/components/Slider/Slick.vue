<template>
  
        <div class="cards">
            <div class="slider">
                <VueSlickCarousel v-bind="settings">
                    <div>
                        <div class="img_box">
                            <img src="../../assets/maldive.jpg" alt="...">
                            <div class="img_title">
                                <p>Maldive</p>
                            </div>
                        </div>

                    </div>
                    <div>
                        <div class="img_box">
                            <img src="../../assets/istanbul.jpg" alt="...">
                            <div class="img_title">
                                <p>Italy</p>
                            </div>
                        </div>
                    </div>
                    <div>
                        <div class="img_box">
                            <img src="../../assets/italy.jpg" alt="...">
                            <div class="img_title">
                                <p>Canada</p>
                            </div>
                        </div>
                    </div>

                </VueSlickCarousel>

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