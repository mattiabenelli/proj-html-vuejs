<script>
import AppNavbar from '../components/AppNavbar.vue'
export default {
  components:{
    AppNavbar
  },
  data(){
    return {
      items:[
        {
          label: 'Home',
          url: '#',
          active: 'false',
          type: 'link'
        },
        {
          label: 'Services',
          url: '#',
          active: 'false',
          type: 'link'
        },
        {
          label: 'About',
          url: '#',
          active: 'false',
          type: 'link'
        },
        {
          label: 'Videos',
          url: '#',
          active: 'true',
          type: 'link'
        },
        {
          label: 'Blog',
          url: '#',
          active: 'false',
          type: 'link'
        },
        {
          label: 'Store',
          url: '#',
          active: 'false',
          type: 'link'
        },
        {
          label: 'schedule a workout',
          url: '#',
          active: 'false',
          type: 'button'
        },
        {
          label: 'icon',
          url: '#',
          active: 'false',
          type: 'link'
        },
        {
          label: 'icon',
          url: '#',
          active: 'false',
          type: 'link'
        }
      ]
    }
  }
}
</script>

<template lang="">
  <header>
    <AppNavbar :navItems="items"/>
    <div class="jumbo">
      <div class="wrapper">
        <div class="jumbo-text">
          <div class="jumbo-text-s-title">Certified fitness professional</div>
          <h1 class="jumbo-text-b-title">Take control of your health</h1>
          <div class="jumbo-text-paragraph">Lorem ipsum dolor sit amet consectetur, adipisicing elit. In a nesciunt aliquid exercitationem quas repellendus saepe assumenda obcaecati voluptatum neque quae molestias ipsa perspiciatis, voluptatibus praesentium architecto dolorum vel ad.</div>
          <div class="jumbo-text-buttons">
            <button>Visit my Youtube channel</button>
            <button>buy avada today</button>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
  @use '../styles/partials/variables' as * ;
  @use '../styles/partials/mixins' as * ;

  .jumbo{
    text-align: left;
    background-image: url('/public//img/banner2-2x.jpg');
    background-size: cover ;
    padding: 100px 0;
    .jumbo-text{
      width: 50%;
      .jumbo-text-s-title{
        color: $PageRed;
        font-size: 30px;
      }
      h1{
        font-size: 70px;
        color: white;
      }
      .jumbo-text-paragraph{
        color: $SmallTxtFontColor;
      }
    }
  }

</style>
<!-- /img/banner2-2x banner -->