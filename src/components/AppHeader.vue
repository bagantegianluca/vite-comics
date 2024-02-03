<script>
export default {
  name: "AppHeader",
  data() {
    return {
      menuList: [
        {
          item: "Character",
          active: false,
        },
        {
          item: "Comics",
          active: true,
        },
        {
          item: "Movies",
          active: false,
        },
        {
          item: "TV",
          active: false,
        },
        {
          item: "Games",
          active: false,
        },
        {
          item: "Collectibles",
          active: false,
        },
        {
          item: "Videos",
          active: false,
        },
        {
          item: "Fans",
          active: false,
        },
        {
          item: "News",
          active: false,
        },
        {
          item: "Shop",
          active: false,
        },
      ],
    };
  },
  methods: {
    toggleActive(index) {
      this.menuList.forEach((item) => (item.active = false));
      this.menuList[index].active = true;
    },
  },
};
</script>

<template>
  <header>
    <div class="container d-flex align-items-center justify-content-between">
      <img src="../assets/img/dc-logo.png" alt="dc-logo" />
      <ul class="d-flex">
        <li
          v-for="(menuItem, i) in menuList"
          :class="menuItem.active ? 'active' : ''"
          @click="toggleActive(i)"
        >
          <a href="#">{{ menuItem.item }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style scoped>
header {
  background: var(--dc-light);
  li {
    margin-inline: 1rem;
    padding-block: 4rem;
    border-bottom: 4px solid transparent;
    transition: all 0.25s;
    a {
      color: var(--dc-dark);
      font-weight: 700;
      text-transform: uppercase;
    }
  }
  li:hover,
  .active {
    border-bottom: 4px solid var(--dc-primary);
  }
}
</style>
