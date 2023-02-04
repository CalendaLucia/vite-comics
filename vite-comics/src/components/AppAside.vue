<script>
 export default {
    name:'AppBonus',
    data() {
        return {

            items : [
                {
                    img: '/src/assets/buy-comics-digital-comics.png',
                    text: "DIGITAL COMICS",
                    url: "#"
                },

                {
                    img: "/src/assets/buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url: "#"
                },
                {
                    img: "/src/assets/buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url: "#"
                },
                {
                    img: "/src/assets/buy-comics-shop-locator.png",
                    text: "COMIC CHOP LOCATOR",
                    url: "#"
                },
                {
                    img: "/src/assets/buy-dc-power-visa.svg",
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

<style lang="css">

body {
    position: relative;
}

#blue-container {
    background-color: #0282f9;
    width: 100%;
    position: absolute;
    top: 180px;
    left: 0px;
}

.icons {
    width: 100%;
    color: white;
    list-style: none;
    display: flex;
    justify-content: center;
    align-items: center; 
}

.icons li {
    display: inline-block;
    padding: 0px 10px;
}

.icons img {
    width: 30px;
    vertical-align: middle;
    padding: 0px 10px;
}

.link {
    text-decoration: none;
}

.text-link {
    font-size: 12px;
    color: white;
    display: inline;
    vertical-align: middle;
    
}
</style>