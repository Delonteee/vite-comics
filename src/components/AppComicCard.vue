<script>
export default {
    data() {
        return {
            
        };
    },
    props: {
        comic: Object
    }
}
</script>

<template>
    <div class="item-comic-container">
        <div class="comic-container">
            <img :src="comic.thumb" :alt="comic.series">
        </div>
        <h3>
            {{comic.series}}
        </h3>
    </div>  
</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;
</style>
