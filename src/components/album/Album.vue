<template>
    <div class="album">
        <div class="album-inner">
            <div class="album-grid">
                <album-cell v-for="cell in getGridCells" :key="cell.id"
                :title="cell.text" 
                :background="cell.background"
                :url="cell.url"
                />
            </div>
        </div>
    </div>
</template>
<script>
import AlbumCell from './AlbumCell.vue'
import albumJson from '../../../config/album.json'

export default {
    name: 'Album',
    components: {
        AlbumCell
    },
    computed: {
        getGridCells() {
            return albumJson.album;
        }
    }
}
</script>
<style lang="scss" scoped>
    .album {
        min-height: 10vh;

        &-inner {
            margin: 1rem auto;
            width: 95%;
        }
        
        .album-grid {
            transform: translateY(-40px);
            display: grid;
            grid-template-columns: repeat(4, 1fr);

            .album-cell {
                min-height: 20vh;
            }
        }
    }
</style>