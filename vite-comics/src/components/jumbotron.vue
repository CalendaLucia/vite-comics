<script>
export default {
    name:'jumbotron',
    data() {
        return {
            
        }
    },
}
</script>

<template>
    <div id="jumbotron">
        <div class="img-jumbo">
          <img src="../assets/img/jumbotron.jpg">
    </div>
    </div>
   
</template>

<style lang="scss" scoped>
@use '../styles/partials/reset.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/media.scss' as *;

#jumbotron {
    width: 100%;
    height: 350px;
    background-color: aqua;

}

    .img-jumbo {
        width: 100%;
        height: 100%;
   
    
        & img {
            @include objectFit;
            object-position: top;
            
        }
    
}

</style>