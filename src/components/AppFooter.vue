<script>
import AppNewVideo from "../components/AppNewVideo.vue";
export default {
  components: {
    AppNewVideo,
  },
  data() {
    return {
      post: [
        {
          label: ">The best protein shake",
          url: "#",
        },
        {
          label: ">Ultimate cardio workout",
          url: "#",
        },
        {
          label: ">New juices avaible now",
          url: "#",
        },
        {
          label: ">Tips to find training partners",
          url: "#",
        },
        {
          label: ">20 best healty recipes",
          url: "#",
        },
      ],
    };
  },
};
</script>

<template lang="">
  <footer>
    <div class="wrapper">
      <div class="row-col">
        <div class="col-30">
          <div class="col-img">
            <img src="/public/img/logo.png" alt="">
          </div>
          <div class="col-text">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Error ullam cupiditate aliquid sequi harum! Possimus soluta necessitatibus commodi unde totam expedita, reprehenderit sapiente vitae quam, perspiciatis similique assumenda sunt? Voluptate.
          </div>
          <div class="col-icons">
            <div class="col-icon"><i class="fa-brands fa-facebook-f"></i></div>
            <div class="col-icon"><i class="fa-brands fa-twitter"></i></div>
            <div class="col-icon"><i class="fa-brands fa-instagram"></i></div>
            <div class="col-icon"><i class="fa-brands fa-youtube"></i></div>
            <div class="col-icon"><i class="fa-brands fa-linkedin-in"></i></div>
          </div> 
        </div>
        <div class="col-30">
          <h3 class="footer-title">RECENT POSTS</h3>
          <AppNewVideo :RecentPost="post"/>
        </div>
        <div class="col-30">
          <h3 class="footer-title">CONTACTS INFORMATIONS</h3>
          <div class="address-place">476 road michigan 48449</div>
          <div>Mobile: 1.800.000.0000</div>
          <div>Email:info@your-company.com</div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.col-icons {
  display: flex;
  justify-content: center;
  gap: 20px;
  color: #cf1b07;
}
.footer-title {
  margin-bottom: 40px;
}
.address-place {
  color: gray;
  margin-bottom: 20px;
}
.col-text {
  color: $SmallTxtFontColor;
  margin: 10px 0 40px;
}
</style>