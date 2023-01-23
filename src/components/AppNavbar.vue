<script>
export default {
    props:{
        navItems: Array
    },
    data(){
        return {
            
        }
    },
    methods:{
        // getType(elem, content){
        //     if(elem === 'link'){
        //         return <a href=""> {{content}} </a>
        //     }
        //     else if(elem === 'button'){
        //         return <button> {{content}} </button>
        //     }
        // }
    }
}
</script>

<template lang="">
    <nav>
      <div class="wrapper">
        <div class="row space-bwt">
          <img src="/public/img/logo.png" alt="">
          <div class="nav-links">
            <ul class="row">
              <!-- <li v-for="(item,index) in navItems" :key="index"> {{ getType(item.type, item.label) }}  </li> -->
            </ul>
          </div>
        </div>
      </div>
    </nav>
</template>

<style lang="scss">
    @use '../styles/partials/variables' as * ;
    @use '../styles/partials/mixins' as * ;
    
    ul{
    list-style-type: none;
    a{
    color: $SmallTxtFontColor;
    text-decoration: none;
    }
  }
  .nav-links{
    .row{
      gap: 10px;
    }
  }
    
</style>