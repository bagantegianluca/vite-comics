<script>
export default {
  name: "AppComic",
  props: {
    comic: Object,
  },
};
</script>

<template>
  <div class="card">
    <img :src="comic.thumb" :alt="comic.series.replaceAll(' ', '_')" />
    <div class="card-info d-flex justify-content-between">
      <span class="series">{{ comic.series }}</span>
      <span class="price">{{ comic.price }}</span>
      <span class="type">{{ comic.type }}</span>
    </div>
  </div>
</template>

<style scoped>
.card {
  height: 100%;
  position: relative;
  cursor: pointer;
  opacity: 0.75;
  transition: all 0.5s;
}

.card:hover {
  opacity: 1;
  scale: 1.1;
}

img {
  max-width: 100%;
  aspect-ratio: 1 / 1.25;
  object-fit: cover;
  object-position: top;
}

.card-info {
  flex-direction: column;
}

.series {
  text-transform: uppercase;
  font-size: 0.8rem;
  font-weight: 700;
}

.price,
.type {
  padding-inline: 0.5rem;
  top: 0;
  transform: translateY(-50%);
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 700;
}

.price {
  position: absolute;
  right: 5px;
  background: yellow;
  color: var(--dc-dark);
}

.type {
  position: absolute;
  left: 5px;
  background: var(--dc-primary);
  color: var(--dc-light);
}
</style>
