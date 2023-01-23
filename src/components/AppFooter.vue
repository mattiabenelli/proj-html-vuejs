<script>
export default {
  
}
</script>

<template lang="">
  <footer>
    <div class="wrapper">
      <div class="row">
        <div class="col-30">
          <div class="col-img">
            <img src="/public/img/logo.png" alt="">
          </div>
          <div class="col-text">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Error ullam cupiditate aliquid sequi harum! Possimus soluta necessitatibus commodi unde totam expedita, reprehenderit sapiente vitae quam, perspiciatis similique assumenda sunt? Voluptate.
          </div>
          <div class="col-icons">
            <div class="col-icon">icon</div>
            <div class="col-icon">icon</div>
            <div class="col-icon">icon</div>
            <div class="col-icon">icon</div>
            <div class="col-icon">icon</div>
          </div> 
        </div>
        <div class="col-30">
          <h1>RECENT POSTS</h1>
          <AppNewVideo />
        </div>
        <div class="col-30"></div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
  @use '../styles/partials/variables' as * ;
  @use '../styles/partials/mixins' as * ;

  .col-icons{
    display: flex;
    justify-content: center;
    gap: 10px;
  }
</style>