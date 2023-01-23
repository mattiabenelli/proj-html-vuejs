<script>
export default {
  
}
</script>

<template lang="">
  <header>
    <nav>
      <div class="wrapper">
        <div class="row space-bwt">
          <img src="/public/img/logo.png" alt="">
          <div class="nav-links">
            <ul class="row">
              <li><a href="#">Home</a></li>
              <li><a href="#">Services</a></li>
              <li><a href="#">About</a></li>
              <li class="active"><a href="#">Videos</a></li>
              <li><a href="#">Blog</a></li>
              <li><a href="#">Store</a></li>
              <li><a href="#"><button>Schedule a workout</button></a></li>
              <li><a href="#">icon</a></li>
              <li><a href="#">icon</a></li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
    <div class="jumbo">
      <div class="wrapper">
        <div class="jumbo-text">

        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
  @use '../styles/partials/variables' as * ;
  @use '../styles/partials/mixins' as * ;
  ul{
    list-style-type: none;
    a{
    color: $NavFontColor;
    text-decoration: none;
    }
  }
  .nav-links{
    .row{
      gap: 10px;
    }
  }
  .jumbo{
    text-align: left;
  }

</style>
<!-- /img/banner2-2x banner -->