<script>
 export default {
    name:'AppFooter',
    data() {
        return {

            socialIcons: [
                {icon: '/src/assets/img/footer-facebook.png'},
                {icon: '/src/assets/img/footer-periscope.png'},
                {icon: '/src/assets/img/footer-pinterest.png'},
                {icon: '/src/assets/img/footer-twitter.png'},
                {icon: '/src/assets/img/footer-youtube.png'},
            ],

            lists: [
                {name:'DC COMICS', link:'#'},
                {name:'Characters', link:'#'},
                {name:'Comics', link:'#'},
                {name:'Movies ', link:'#'},
                {name:'TV',link:'#'},
                {name:'Games',link:'#'},
                {name:'Videos', link:'#'},
                {name:'News', link:'#'},
            ],

            other_list_1: [
                {name: 'SHOP', link: '#' },
                {name: 'Shop DE', link: '#' },
                {name: 'Shop DC Collectibles', link: '#'},
           ],

           other_list_2: [
                {name: 'DC', link: '#' },
                {name: 'Terms Of Use', link: '#' },
                {name: 'Privacy policy (New)', link: '#'},
                {name: 'Ad Choices', link: '#'},
                {name: 'Advertising', link: '#'},
                {name: 'Jobs', link: '#'},
                {name: 'Subscriptions', link: '#'},
                {name: 'Talent Workshops', link: '#'},
                {name: 'CPSC Certificates', link: '#'},
                {name: 'Ratings', link: '#'},
                {name: 'Shop Help', link: '#'},
                {name: 'Contact Us', link: '#'},
                
           ],

            other_list_3: [
                {name: 'SITES', link: '#'},
                {name: 'DC', link: '#'},
                {name: 'MAD Magazine', link: '#'},
                {name: 'DC Kids', link: '#'},
                {name: 'DC Universe', link: '#'},
                {name: 'DC Power Visa', link: '#'},
           ],

           
            
        }
    
  },

  computed: {
    all_lists() {
      return [this.lists, this.other_list_1, this.other_list_2, this.other_list_3];
    },
  },
}
</script>

<template>
   <footer>
     <div id="credits">
        <section class="DC-logo">
            <img class="DC-bg" src="../assets/img/dc-logo-bg.png">
        </section>
        <section class="column">
          <ul :class="index === 0 || index === 1 ? 'menu-second' : 'menu'" v-for="(lists, index) in all_lists" :key="index">
             <li v-for="(item, index) in lists" :key="item.id">
                <a :class="index === 0 ? 'title' : 'item-credits'" :href="item.link"> {{ item.name }}</a>
             </li>
           </ul>
        </section>
     </div>
     <div id="info">
        <div class="sign-up">
           <button>
            SIGN-UP NOW!
           </button>
        </div>
        <div class="follow-us">
            <div>
               <h6>FOLLOW US</h6>
            </div>
        <div class="icon">
            <ul class="menu-icons">
               <li class="icons" v-for="icon in socialIcons" :key="icon.id">
                  <img class="img" :src="icon.icon">
               </li>
            </ul>
        </div>
    </div>
</div>
</footer>
</template>

<style lang="scss" >  
@import '../styles/partials/footer.scss' ;
</style>