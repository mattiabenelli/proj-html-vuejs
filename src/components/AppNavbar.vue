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
      getType(elem, content, url, active){
        if(elem === 'button'){
            return `<button> ${content} </button>`
        }
        if(elem === 'link' && active == true){
            return `<a class="active" href="${url}"> ${content} </a>`
        }
          else{
            return `<a href="${url}"> ${content} </a>`
        }
      }
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
              <li v-for="(item,index) in navItems" :key="index" v-html="getType(item.type, item.label, item.url, item.active)" >  </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
</template>

<style lang="scss">
    @use '../styles/partials/variables' as * ;
    @use '../styles/partials/mixins' as * ;
  
    .nav-links{
    .row{
      gap: 10px;
    }
    ul{
    list-style-type: none;
      a{
        color: $SmallTxtFontColor;
        text-decoration: none;
    }
    }
  }
    
</style>