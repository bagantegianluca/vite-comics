<script>
export default {
  name: "AppFooterMenu",
  props: {
    menu: Object,
  },
};
</script>

<template>
  <div class="col">
    <ul>
      <h3>{{ menu.title }}</h3>
      <li v-for="item in menu.items">
        <a href="#">{{ item }}</a>
      </li>
    </ul>
  </div>
</template>

<style>
h3 {
  text-transform: uppercase;
}

a {
  font-size: 0.8rem;
  color: var(--dc-gray);
  transition: all 0.25s;
}

a:hover {
  color: var(--dc-light);
}

.col {
  padding: 0 1rem;
}
</style>
