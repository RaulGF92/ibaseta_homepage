<template src="./template.html"></template>
<script>
import mainJson from '../../../config/main.json'

export default {
    name: 'HomePage',
    data() {
        return {
            url : mainJson.portada_imagen,
            showMenu: false,
            name: mainJson["datos-personales"].nombre,
            phone: mainJson["datos-personales"].telefono,
            emai: mainJson["datos-personales"].email,
            botonPrincipal: mainJson["boton-principal"]
        }
    },
    computed: {},
    methods: {
        onNovedadesClick() {
            window.open(this.botonPrincipal.url,"_blank")
        },
        goTo(path) {
            this.showMenu = false
            window.location = path
        }
    }
}
</script>
<style lang="scss" src="./styles.scss"  scoped></style>