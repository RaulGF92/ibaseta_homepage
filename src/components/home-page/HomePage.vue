<template src="./template.html"></template>
<script>
import mainJson from '../../../config/main.json'

export default {
    name: 'HomePage',
    data() {
        return {
            url : mainJson.portada_imagen,
            showMenu: false
        }
    },
    computed: {},
    methods: {
        onNovedadesClick() {
            window.open("https://www.flickr.com/photos/ibaseta2/albums/72157656150903658","_blank")
        },
        goTo(path) {
            this.showMenu = false
            window.location = path
        }
    }
}
</script>
<style lang="scss" src="./styles.scss"  scoped></style>