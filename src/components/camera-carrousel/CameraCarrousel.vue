<template>
    <div class="camera-carrousel">
        <div class="header">
            <h1>Mis Camaras</h1>
            <div style="min-width:20px;" />
            <sub style="color: lightgray;">( Pulsa sobre ellas para conocer la especificación )</sub>
        </div>
        <br>
        <carousel class="carrousel" autoplay>
        <slide v-for="camera in getCameras" :key="camera.id">
            <img :src="getImg(camera.img)" @click="onClick(camera)"/>
        </slide>
        </carousel>
    </div>
</template>
<script>
import { Carousel, Slide } from 'vue-carousel';
import configJson from '../../../config/main.json'

export default {
    name: 'CameraCarrousel',
    components: {
        Carousel,
        Slide
    },
    computed: {
        getCameras() {
            return configJson.cameras
        }
    },
    methods: {
        onClick(camera) {
            window.open(camera.url, '_blank')
        },
        getImg(url) {
            return require(url)
        }
    }
}
</script>
<style lang="scss">
    .camera-carrousel {
        margin: auto;
        width: 95%;
        .carrousel {
            margin: auto;
            width: 90%;
        }

        img {
            width: 100%;
            height: auto;
            max-width: 30vw;
        }

        .header {
            display: flex;
            flex-direction: row;
            align-content: space-between;
            align-items: center;
        }
    }

</style>