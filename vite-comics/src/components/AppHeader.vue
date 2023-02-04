<script>
import jumbotron from './jumbotron.vue';
export default {
    name: "AppHeader",
    components: {
         jumbotron
    },
    data() {
        return {
            items: [
                {
                    name: "CHARACTERS",
                    link: "#"
                },
                {
                    name: "COMICS",
                    link: "#"
                },
                {
                    name: "MOVIES",
                    link: "#"
                },
                {
                    name: "TV",
                    link: "#"
                },
                {
                    name: "GAMES",
                    link: "#"
                },
                {
                    name: "COLLECTIBLES",
                    link: "#"
                },
                {
                    name: "VIDEOS",
                    link: "#"
                },
                {
                    name: "FANS",
                    link: "#"
                },
                {
                    name: "NEWS",
                    link: "#"
                },
                {
                    name: "SHOP",
                    link: "#"
                }
            ]
        };
    },
}
</script>

<template>
     <header>
        <div id="container">
          <div class="logo">
             <div class="img">
                <img src="../assets/img/dc-logo.png" alt="logo">
             </div>
          </div>
        <div class="nav-bar">
            <ul class="menu">
                <li class="item" v-for="item in items" :key="item.id">
                    <a :href="item.link"> {{ item.name }}</a> 
                </li>
            </ul>
        </div>
        </div>
        <div id="jumbotron">
            <jumbotron/>
        </div>
    </header>
</template>

<style lang="scss" >
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/reset.scss' as *;

#container, .logo, .navbar {
  @include flex(space-around, center);
}

#container {
     width: 100%;
     padding: 10px 0px;
     background-color:#ffffff;
     position: relative;
     z-index: 3;
   

     .logo {
        width: 20%;
        justify-content: flex-end;
     }

     .img {
        width: 50px;
        height: 50px;

        img {
            @include objectFit;
        }
     }

  }

.nav-bar {
   width: 80%;
   justify-content: flex-end;

   .menu {
      display: flex;
      justify-content: center;

      .item {
        @include listStyle (inline-block);
        font-size:12px ;
        padding:10px 10px;
        border-bottom: 2px solid transparent;
        transition: border-bottom 0.3s ease;

        &:hover {
          border-bottom: 2px solid #0282f9;
        }

           a {
             color: black;
             @include linkStyle;

               &:hover {
                 color: $primary-color;
               }
            }
      }   

   }
}


</style>

