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
      </div>
    </div>
  </main>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.rainbow-section {
  background: linear-gradient(135deg, #4257ef, #6b0c7a, #bc0428);
  height: 400px;
}
.card-section {
  width: 100%;
}
</style>