<script>
import AppFooterMenu from "./AppFooterMenu.vue";

export default {
  name: "AppFooterTop",
  components: {
    AppFooterMenu,
  },
  data() {
    return {
      menus: [
        {
          title: "DC Comics",
          items: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "Shop",
          items: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          title: "DC",
          items: [
            "Terms Of Use",
            "Privacy Policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "Sites",
          items: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-top">
    <div class="container">
      <div class="row d-flex">
        <AppFooterMenu v-for="menu in menus" :menu="menu"></AppFooterMenu>
      </div>
    </div>
  </div>
</template>

<style scoped>
.footer-top {
  background: url("../assets/img/footer-bg.jpg");
  background-size: cover;
}

.container {
  background: url("../assets/img/dc-logo-bg.png");
  background-repeat: no-repeat;
  background-position-x: right;
  background-position-y: center;
  padding-block: 3rem;
}

.row {
  margin: 0 -1rem;
}
</style>
