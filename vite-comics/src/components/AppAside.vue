<script>
 export default {
    name:'AppBonus',
    data() {
        return {

            items : [
                {
                    img: '/src/assets/img/buy-comics-digital-comics.png',
                    text: "DIGITAL COMICS",
                    url: "#"
                },

                {
                    img: "/src/assets/img/buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url: "#"
                },
                {
                    img: "/src/assets/img/buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url: "#"
                },
                {
                    img: "/src/assets/img/buy-comics-shop-locator.png",
                    text: "COMIC CHOP LOCATOR",
                    url: "#"
                },
                {
                    img: "/src/assets/img/buy-dc-power-visa.svg",
                    text: "DC POWER VISA",
                    url: "#"
                }

            ]

        }
    
  }
}
</script>

<template>
    <div id="blue-container">
       <ul class="icons">
         <li v-for="item in items" :key="item.id">
            <a class="link" :href="item.url">
                <img :src="item.img">
                <p class="text-link">{{ item.text }}</p>
            </a>
         </li>
       </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/reset.scss' as *;

#blue-container {
    background-color:$primary-color;
    width: 100%;
    position: absolute;
    bottom: 0px;
    left: 0px;
    padding: 30px 0px;

    .icons {
       width: 100%;
       color: white;
       @include listStyle (inline-block);
       @include flex (center, center);

       & li {
          padding: 0px 10px;
          & .link {
               @include linkStyle;
            }

          & img {
             width: 65px;
             vertical-align: middle;
             padding: 0px 10px;
          }
          .text-link {
              font-size: 12px;
              color: white;
              display: inline;
              vertical-align: middle;
            }
       }
     }
}
</style>