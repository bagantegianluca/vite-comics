<script>
export default {
  name: "AppFooterBottom",
  data() {
    return {
      socials: [
        {
          title: "facebook",
          img: "footer-facebook.png",
        },
        {
          title: "twitter",
          img: "footer-twitter.png",
        },
        {
          title: "youtube",
          img: "footer-youtube.png",
        },
        {
          title: "pinterest",
          img: "footer-pinterest.png",
        },
        {
          title: "periscope",
          img: "footer-periscope.png",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-bottom">
    <div class="container d-flex align-items-center justify-content-between">
      <a href="#" class="btn">Sign-up now!</a>
      <div class="social-links d-flex align-items-center">
        <span>Follow us</span>
        <ul class="d-flex">
          <li v-for="social in socials">
            <a href="#"
              ><img :src="'/src/assets/img/' + social.img" :alt="social.title"
            /></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.footer-bottom {
  background: var(--dc-l-dark);
  padding-block: 2rem;
}

.btn {
  display: inline-block;
  font-size: 1rem;
  font-weight: bold;
  text-transform: uppercase;
  color: var(--dc-light);
  padding: 1rem;
  border: 1px solid var(--dc-primary);
  transition: all 0.5s;
}

.btn:active {
  background: var(--dc-primary);
  color: var(--dc-light);
}

span {
  text-transform: uppercase;
  color: var(--dc-primary);
  font-weight: bold;
  font-size: 1.25rem;
}

ul {
  margin-left: 1rem;
}

li {
  margin-left: 0.75rem;
}
</style>
