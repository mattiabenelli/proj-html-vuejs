<script>
export default {
    props:{
        navItems: Array,
    },
  }

</script>

<template lang="">
    <nav>
      <div class="wrapper">
        <div class="row space-bwt">
          <img src="/public/img/logo.png" alt="">
          <div class="nav-links">
            <ul class="row">
              <li v-for="(item,index) in navItems" :key="index">
                <a :href="item.url">{{ item.label }}</a>
                <span v-if="item.new" class="newSection">new</span>
                <ul v-if="item.subMenu">
                  <li v-for="(items,index) in item.subMenu" :key="index">{{ items }}</li>
                </ul>
              </li>
              <li><button>schedule a workout</button></li>  
              <li class="header-icon"><a href="#">icon</a></li>
              <li class="header-icon"><a href="#">icon</a></li>
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
    .newSection{
      background-color: yellow;
      padding: 3px;
      color: black;
      border-radius: 5px;
      margin-left: 5px;
    }
  }
    
</style>