<script>
import AppCards from './AppCards.vue'
import comicData from '../comicData.json'
export default {
    name:'AppMain',
    data() {
        return { 
            comicData
        }
    },
    components: {
        AppCards
    }
}
</script>

<template>
    <main>
        <div id="content">
            <div class="cards">
                <AppCards :comics="comicData" />
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
        padding: 30px 20px 30px 20px;

        .cards {
            width: 70%;
            margin: 0 auto;
            display: flex;
            justify-content: space-around;
            align-items: center;
            flex-wrap: wrap;
          
        }

    }
}
</style>