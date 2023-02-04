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

#jumbotron {
    #jumbotron {
    width: 100%;
    padding: 40px 0px;

    .img-jumbo {
        width: 100%;
        height: 100px;

        &img {
            width: 100%;
            object-fit: cover;
        }
    }
}
}

</style>