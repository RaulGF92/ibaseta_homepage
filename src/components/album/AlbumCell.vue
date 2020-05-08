<template>
    <div class="album-cell">
        <div class="album-cell_inner" @click="onClick()">
            <img :src="background" />
            <div class="title">
                <label>{{title}}</label>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'AlbumCell',
    props: {
        title: {
            type: String,
            required: true
        },
        background: {
            type: String,
            required: true
        },
        url: {
            type: String,
            required: true
        }
    },
    methods: {
        onClick() {
            window.open(this.url, '_blank')
        }
    }
}
</script>
<style lang="scss" scoped>
    .album-cell {
        width: 100%;
        height: 100%;

        &_inner {
            position: relative;
            overflow: hidden;
            background-color: var(--secondary-color,#fff);
            margin: auto;
            width: 85%;
            height: 90%;
            max-height: 200px;

            img {
                width: 100%;
                height: 100%;
            }

            .title {
                height: 100%;
                width: 100%;
                position: absolute;
                top: 0;
                z-index: 2;
                display:flex;
                align-items: center;
                background-color: rgba(#2f2f2f, 0.2);
                cursor: pointer;
                
                label {
                    width: 100%;
                    text-align: center;
                    color: white;
                }

                &:hover {
                    background-color: rgba(#2f2f2f, 0.8);
                }
            }
        }
    }
</style>