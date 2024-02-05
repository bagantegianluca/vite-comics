<script>
export default {
  name: "AppBanner",
  data() {
    return {
      bannerList: [
        {
          title: "Digital Comics",
          img: "buy-comics-digital-comics.png",
        },
        {
          title: "DC merchandise",
          img: "buy-comics-merchandise.png",
        },
        {
          title: "Subscription",
          img: "buy-comics-subscriptions.png",
        },
        {
          title: "Comic Shop Locator",
          img: "buy-comics-shop-locator.png",
        },
        {
          title: "DC Power Visa",
          img: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="container">
    <ul class="d-flex justify-content-between">
      <li class="d-flex align-items-center" v-for="bannerItem in bannerList">
        <img
          :src="'/src/assets/img/' + bannerItem.img"
          :alt="bannerItem.title.replaceAll(' ', '_')"
        />
        <span>{{ bannerItem.title }}</span>
      </li>
    </ul>
  </div>
</template>

<style scoped>
ul {
  padding: 3rem 0;
}

li {
  cursor: pointer;
  transition: all 0.5s;
  border-bottom: 2px solid transparent;
  padding-block: 0.25rem;
}

li:hover {
  border-bottom: 2px solid var(--dc-light);
}

img {
  width: 50px;
  height: 50px;
  object-fit: contain;
}
span {
  display: inline-block;
  /* white-space: nowrap; */
  text-transform: uppercase;
  margin-left: 0.5rem;
}
</style>
