<script>
import AppNavbar from "../components/AppNavbar.vue";
export default {
  components: {
    AppNavbar,
  },
  data() {
    return {
      items: [
        {
          label: "Home",
          url: "#",
          active: true,
          new: false,
        },
        {
          label: "Services",
          url: "#",
          active: false,
          new: false,
          subMenu: [
            {
              subMenulabel: "All services",
              subMenuUrl: "#",
            },
            {
              subMenulabel: "Service single page",
              subMenuUrl: "#",
            },
          ],
        },
        {
          label: "About",
          url: "#",
          active: false,
          new: false,
          subMenu: [
            {
              subMenulabel: "About Me",
              subMenuUrl: "#",
            },
            {
              subMenulabel: "Our Sponsor",
              subMenuUrl: "#",
            },
            {
              subMenulabel: "Contact",
              subMenuUrl: "#",
            },
          ],
        },
        {
          label: "Videos",
          url: "#",
          active: false,
          new: false,
          subMenu: [
            {
              subMenulabel: "All Playlist",
              subMenuUrl: "#",
            },
            {
              subMenulabel: "Playlist Page",
              subMenuUrl: "#",
            },
            {
              subMenulabel: "Video Single Page",
              subMenuUrl: "#",
            },
          ],
        },
        {
          label: "Blog",
          url: "#",
          active: false,
          new: false,
        },
        {
          label: "Store",
          url: "#",
          active: false,
          new: true,
          subMenu: [
            {
              subMenulabel: "Simple Product",
              subMenuUrl: "#",
            },
            {
              subMenulabel: "Variable Product",
              subMenuUrl: "#",
            },
          ],
        },
      ],
    };
  },
};
</script>

<template lang="">
  <header>
    <AppNavbar :navItems="items"/>
    <div class="jumbo">
      <div class="wrapper row space-bwt">
        <div class="jumbo-text animate">
          <div class="jumbo-text-s-title">Certified fitness professional</div>
          <h1 class="jumbo-text-b-title">Take control of your health</h1>
          <div class="jumbo-text-paragraph">Lorem ipsum dolor sit amet consectetur, adipisicing elit. In a nesciunt aliquid exercitationem quas repellendus saepe assumenda obcaecati voluptatum neque quae molestias ipsa perspiciatis, voluptatibus praesentium architecto dolorum vel ad.</div>
          <div class="jumbo-text-buttons">
            <button class="blue-red-btn btn-big"><i class="icon fa-brands fa-youtube"></i>Visit my Youtube channel</button>
            <button class="black-white-btn btn-big">buy avada today &#10132;</button>
          </div>
        </div>
        <button class="video-btn video-btn-header animate"><i class="fa-solid fa-play"></i></button>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.jumbo {
  text-align: left;
  background: linear-gradient(to right, black 40%, transparent 90%),
    url("/public//img/slider82x-scaled.jpg");
  background-size: cover;
  padding: 150px 0 200px;
  .icon {
    margin-right: 10px;
  }
  .jumbo-text {
    width: 50%;
    .jumbo-text-s-title {
      color: $PageRed;
      font-size: 30px;
    }
    h1 {
      font-size: 70px;
      color: white;
    }
    .jumbo-text-paragraph {
      color: $SmallTxtFontColor;
    }
    .jumbo-text-buttons {
      padding: 20px 0;
      button {
        margin-right: 20px;
      }
    }
  }
}
</style>
