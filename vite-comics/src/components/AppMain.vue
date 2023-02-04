<script>
export default {
    name:'AppMain',
    data() {
        return {
            
        }
    },
}
</script>

<template>
    <main>
        <div id="content">
            <div class="text">
                <h5>-- Content goes here --  </h5>
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
}
.text {
    background-color: black;
    padding: 20px 0px;
}
</style>