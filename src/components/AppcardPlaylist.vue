<script>
export default {
  props: {
    cardPlaylist: Array,
  },
};
</script>

<template lang="">
    <div v-for="(item,index) in cardPlaylist" :key="index" class="card-playlist">
        <a :href="item.url"><img :src="item.img" alt=""></a>
        <button class="video-btn video-btn-card"><i class="fa-solid fa-play"></i></button>
        <div class="card-playlist-text">
            <div class="card-playlist-text-title">{{ item.title }}</div>
            <div class="card-playlist-text-subtitle">{{ item.subtitle }}</div>
        </div>
    </div>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;
.card-playlist {
  width: 30%;
  position: relative;
  text-align: center;
  a {
    width: 100%;
    height: 100%;
  }
  img {
    width: 100%;
    height: 100%;
    border-radius: 5px 5px 30px 5px;
    object-fit: contain;
  }
  .video-btn-card {
    position: absolute;
    left: 50%;
    top: 40%;
    transform: translate(-50%, -50%);
  }
  .card-playlist-text {
    padding: 20px 0;
    .card-playlist-text-title {
      font-weight: bold;
      font-size: 20px;
    }
    .card-playlist-text-subtitle {
      color: $blueBtn;
      font-size: 15px;
    }
  }
}
</style>