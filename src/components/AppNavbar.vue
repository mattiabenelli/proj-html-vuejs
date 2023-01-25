<script>
export default {
  props: {
    navItems: Array,
  },
};
</script>

<template lang="">
    <nav>
      <div class="wrapper">
        <div class="row space-bwt">
          <img src="/public/img/logo.png" alt="">
          <div class="nav-links">
            <ul class="row">
              <li class="dropdown" v-for="(item,index) in navItems" :key="index">
                <a :href="item.url" v-bind:class="(item.active == true) ? 'active' : ''">{{ item.label }}<span v-if="item.new" class="newSection" >new</span></a>
                <ul class="dropdown-content" v-if="item.subMenu">
                  <li v-for="(items,index) in item.subMenu" :key="index"><a :href="items.subMenuUrl">{{ items.subMenulabel }}</a></li>
                </ul>
              </li>
              <li><button class="blue-red-btn btn-small">schedule a workout</button></li>  
              <li class="header-icon"><a href="#"><i class="fa-solid fa-magnifying-glass"></i></a></li>
              <li class="header-icon"><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.nav-links {
  .row {
    gap: 50px;
  }
  ul {
    list-style-type: none;
    a {
      color: $SmallTxtFontColor;
      text-decoration: none;
    }
  }
  .newSection {
    background-color: yellow;
    padding: 1px 3px 4px 3px;
    color: black;
    border-radius: 5px;
    margin-left: 5px;
  }
}
.dropdown {
  position: relative;
  display: inline-block;
  height: 100%;
}
.dropdown-content {
  display: none;
  position: absolute;
  background-color: black;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
  a {
    color: $SmallTxtFontColor !important;
  }
}
.dropdown-content li {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}
.dropdown:hover .dropdown-content {
  display: block;
  transition-duration: 0.2s;
}
</style>