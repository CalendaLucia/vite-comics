<script>
export default {
    name:'AppCards',
    props: ['comics'],
};
</script>

<template>
    <div class="comics" v-for="comic in comics" :key="comic.id">
      <img :src="comic.thumb" />
      <div class="series">
         <p class="text">{{ comic.series }}</p>
      </div>
    </div>
    <div class="more">
      <button>
        LOAD MORE
      </button>
    </div>
   
</template>

<style lang="scss">
@use '../styles/partials/reset.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

   .comics {
       width: calc((100% / 6) - 10px);
       height: 170px;
       margin: 30px 0px;

       img {
         width: 100%;
         height: 100%;
         object-fit: cover;
         object-position: top;
       }

       .series {
        padding: 5px 0px;
         
         .text {
            color: white;
       }
          
       }   
  }

  .more {
    width: 50%;
    margin: 0 auto;
    padding: 40px 0px;
    @include flex (center, center);
    align-self: flex-end;

       & button {
        @include button (10px 50px, 13px, none, white, 1px solid black);
        background-color: $primary-color;
        border-radius: 3px;
        font-size: 8px;

         &:hover {
          cursor: pointer;
         }
        
       }
    
  }

   

</style>