<template>
    <section id="showcase" class="pa-0 ma-0">
        <v-carousel>
            <v-carousel-item :src="bgImage">

            </v-carousel-item>
            <v-carousel-item>
                <v-sheet height="100%">
                    <v-img contain :src="bgImage1" gradient="rgba(0,0,0,0.5),rgba(0,0,0,0.5)">

                    </v-img>
                </v-sheet>
            </v-carousel-item>
        </v-carousel>
    </section>
</template>

<script>
/* eslint-disable */
export default {
    data(){
        return{
            bgImage: require('@/assets/images/bg0.jpg'),
            bgImage1: require('@/assets/images/bg1.jpg'),
            bgGradient: "linear-gradient(red,blue)"
        }
    },
    mounted(){
        //document.querySelector('#showcase').style.background = 'url('+bgImage+') center center / cover no-repeat,'+bgGradient+' no-repeat';
    }
}

</script>
<style language="scss" scoped>
    :root{
        --bg-image:url('{{ bgImage }}')
    }
    #showcase{
        width: 100%;
        height: 90vh;
        background-size: cover;
        background-position: center;
    }
</style>
