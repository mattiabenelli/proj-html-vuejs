<script>
export default {
  props: {
    cardRainbow: Array,
  },
};
</script>

<template lang="">
    <div v-for="(item,index) in cardRainbow" :key="index" class="card-rainbow">
        <a :href="item.url"><img :src="item.img" alt=""></a>
        <div class="card-rainbow-text">
            <div class="card-rainbow-text-title">{{ item.title }}</div>
            <div class="card-rainbow-text-subtitle">{{ item.subtitle }}</div>
        </div>
    </div>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.card-rainbow {
  width: 30%;
  position: relative;
  a {
    width: 100%;
    height: 100%;
  }
  img {
    width: 75%;
    height: 75%;
    box-shadow: 20px 20px 50px 10px black inset;
  }
  .card-rainbow-text {
    position: absolute;
    bottom: 30px;
    left: 40px;
    .card-rainbow-text-title {
      color: white;
      font-size: 25px;
    }
    .card-rainbow-text-subtitle {
      color: $yellowPage;
      font-size: 20px;
    }
  }
}
</style>