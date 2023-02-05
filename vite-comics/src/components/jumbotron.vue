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
    <div class="img-jumbo">
        <img src="../assets/img/jumbotron.jpg">
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/reset.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

  

    .img-jumbo {
        width: 100%;
        height: 50vh;
        background-color: rebeccapurple;
   
    
        &img {
            @include objectFit;
            
        }
    
}

</style>