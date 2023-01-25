<script>
import AppcardRainbow from "../components/AppcardRainbow.vue";
export default {
  components: {
    AppcardRainbow,
  },
  data() {
    return {
      cardsRainbow: [
        {
          img: "/public/img/service6-2x.jpg",
          url: "#",
          title: "Crossfit workout",
          subtitle: "Push your limit",
        },
        {
          img: "/public/img/box1-2x.jpg",
          url: "#",
          title: "New gym apparel",
          subtitle: "Look good, feel good",
        },
        {
          img: "/public/img/box3-2x.jpg",
          url: "#",
          title: "Team training",
          subtitle: "Find a partner",
        },
      ],
    };
  },
};
</script>

<template lang="">
  <main>
    <div class="rainbow-section">
      <div class="wrapper">
        <div class="card section">
          <div class="row space-bwt">
            <AppcardRainbow :cardRainbow="cardsRainbow"/>
          </div>
        </div>
        <div class="caption-section">
          <div class="caption-section-paragraph">"Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem sunt deleniti maxime unde cumque ea, ullam iusto repudiandae, est eaque asperiores commodi excepturi. Voluptatem mollitia incidunt inventore unde sit illo!</div>
          <div class="caption-section-person row jsy-center">
            <div class="caption-section-person-img">
              <img src="/public/img/avatar-1-2x.jpg" alt="">
            </div>
            <div class="caption-section-person-name">Brad Johnson</div>
            <div class="caption-section-person-place">Las Vegas</div>
          </div>
        </div>
      </div>
    </div>
    <div class="video-section row space-bwt">
      <div class="youtube-section-video">
              <img src="public/img/service15-2x.jpg" alt="">
              <button class="video-btn video-btn-main"><i class="fa-solid fa-play"></i></button>
        </div>
        <div class="wrapper">
          <div class="youtube-section">
            <div class="youtube-section-text">
              <div class="youtube-section-text-stitle">Tune up your workouts</div>
              <div class="youtube-section-text-btitle">The best health & fitness advice online</div>
              <div class="youtube-section-text-paragraph">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam accusantium, quod culpa dolores adipisci provident aspernatur. Exercitationem, vero recusandae at sapiente laboriosam suscipit similique harum, culpa consectetur facilis maiores sint! </div>
              <button class="yt-btn btn-big"><i class="icon fa-brands fa-youtube"></i>Visit my Youtube channel</button>
            </div>
        </div>
      </div>
    </div>
    <div class="playlist-section">
      <div class="wrapper">
        <div class="playlist-tag">

        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.rainbow-section {
  background: linear-gradient(135deg, #4257ef, #6b0c7a, #bc0428);
  padding-bottom: 50px;
  .card-section {
    width: 100%;
  }
  .caption-section {
    padding: 100px;
    width: 80%;
    text-align: center;
    margin: 0 auto;
    img {
      width: 60px;
      height: 60px;
      border-radius: 50%;
    }
    .caption-section-paragraph {
      font-size: 40px;
      color: white;
    }
    .caption-section-person {
      padding: 20px 0;
      .caption-section-person-name {
        color: white;
        padding: 0 20px;
        font-size: 20px;
      }
      .caption-section-person-place {
        color: $SmallTxtFontColor;
      }
    }
  }
}
.video-section {
  .youtube-section-video {
    width: 70%;
    position: relative;
    img {
      width: 100%;
      height: 700px;
      object-fit: cover;
      border-radius: 5px 5px 40px 5px;
      transform: translateY(-50px);
    }
    .video-btn-main {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
    }
  }
  .youtube-section {
    width: 80%;
    margin: 0 auto;
    .youtube-section-text {
      height: 600px;
      .youtube-section-text-stitle {
        color: $blueBtn;
        font-size: 25px;
        font-weight: bold;
        padding-bottom: 40px;
      }
      .youtube-section-text-btitle {
        font-size: 70px;
      }
      .youtube-section-text-paragraph {
        color: gray;
        padding: 40px 0;
        font-size: 20px;
      }
      .yt-btn {
        background-color: #e20813;
        border: #e20813;
        color: white;
      }
    }
  }
}
</style>