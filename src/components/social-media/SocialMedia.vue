<template src="./template.html"></template>
<script>
import mainJson from '../../../config/main.json'
export default {
    name: 'SocialMedia',
    methods: {
        onClick(media) {
            window.open(mainJson["redes-sociales"][media],"_blank")
        }
    }
}
</script>
<style lang="scss" src="./styles.scss"></style>