<script>
import AppCards from './AppCards.vue'
import comicData from '../comicData.json'
import AppAside from './AppAside.vue'
export default {
    name:'AppMain',
    data() {
        return { 
            comicData
        }
    },
    components: {
        AppCards,
        AppAside
    }
}
</script>

<template>
    <main>
        <div id="content">
            <div class="cards">
                <AppCards :comics="comicData" />
                <AppAside/>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/reset.scss' as *;

main  {
    position: relative;
    z-index: 3;

    #content {
        background-color: black;
        padding: 30px 20px 100px 20px;

        .cards {
            width: 70%;
            margin: 0 auto;
            @include flex (space-around, center);
            flex-wrap: wrap;
        }

    }
}
</style>