<script setup>
import { ref } from "vue";
import PageTitle01 from "../components/PageTitle01.vue";
const pageTitleContnet = ref({
  name: "about",
  title: "認識崴傑",
  subtitle: "在崴傑，您對家的夢想，由我們守護。",
});

const contentText = ref([
  "崴傑傳承家族辦公室提供一站式財富管理服務平台，",
  "動產與不動產顧問諮詢，還有財務規劃及信託傳承，",
  "為您的財富把關並保護您的個人資訊。",
  "在崴傑，您對家的夢想，由我們守護。",
]);
</script>
<style lang="scss" scoped>
.about {
  &__titleBox {
    background-image: url("../assets/images/About.png");
  }
  &__content {
    padding: 60px 16px 120px;
    img {
      width: 100%;
    }
    p {
      font-family: "Noto Sans TC";
      font-style: normal;
      font-weight: 400;
      font-size: 16px;
      line-height: 40px;
      letter-spacing: 0.2px;
      color: #373f41;
      margin-bottom: 0;
    }
  }
  .row {
    margin-top: -30px;
  }
  &__info {
    margin-top: 30px;
  }
}
@media screen and (min-width: 1200px) {
  .about {
    &__content {
      padding: 50px 150px 200px;
    }
  }
}
</style>
<template>
  <div class="about">
    <PageTitle01 class="about__titleBox" :page="pageTitleContnet" />
    <div class="about__content">
      <div class="row">
        <div class="col-12 col-xl-6 about__info">
          <img src="../assets/images/Aboutsub.png" alt="" />
        </div>
        <div class="col-12 col-xl-6 about__info">
          <p v-for="text in contentText">{{ text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
