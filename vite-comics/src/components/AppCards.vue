<script>
export default {
    name:'AppCards',
    props: ['comics'],
};
</script>

<template>
    <div class="comics" v-for="comic in comics" :key="comic.id">
      <img :src="comic.thumb" />
    </div>
       <!-- <p>{{ comic.series }}</p> -->
  

</template>

<style lang="scss">
@use '../styles/partials/reset.scss' as *;
@use '../styles/partials/mixins.scss' as *;



   .comics {
       width: calc((100% / 6) - 10px);
       height: 170px;
       margin: 15px 0px;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: top;
    }
  }

   

</style>