<template>
    <div class="camera-carrousel">
        <h2>Mis Camaras</h2>
        <hr>
        <carousel class="carrousel">
        <slide>
            Slide 1 Content
        </slide>
        <slide>
            Slide 2 Content
        </slide>
            <slide>
            Slide 2 Content
        </slide>
        </carousel>
    </div>
</template>
<script>
import { Carousel, Slide } from 'vue-carousel';

export default {
    name: 'CameraCarrousel',
    components: {
        Carousel,
        Slide
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
    }

</style>