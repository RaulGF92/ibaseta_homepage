<template src="./template.html"></template>
<script>
import mainJson from '../../../config/main.json'

export default {
    name: 'HomePage',
    data() {
        return {
            url : mainJson.portada_imagen
        }
    },
    computed: {}
}
</script>
<style lang="scss" src="./styles.scss"  scoped></style>