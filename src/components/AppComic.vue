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
    <img :src="comic.thumb" :alt="comic.series.replace(' ', '_')" />
    <div class="card-info d-flex justify-content-between">
      <span class="series">{{ comic.series }}</span>
      <span class="price">{{ comic.price }}</span>
      <span class="type">{{ comic.type }}</span>
    </div>
  </div>
</template>

<style scoped>
.card {
  position: relative;
  height: 100%;
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

.series,
.price,
.type {
  padding-inline: 0.5rem;
  border-radius: 10px;
  top: 10px;
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 700;
}

.price {
  position: absolute;
  right: 10px;
  background: yellow;
  color: var(--dc-dark);
}

.type {
  position: absolute;
  left: 10px;
  background: var(--dc-primary);
  color: var(--dc-light);
}
</style>
