<template>
  <footer>
    <a
     class="footer-nav back"
     @click="goBack"
    >
      <div class="footer-nav-icon">
        <fa-icon :icon="['fa-solid', 'turn-up']" rotation="270" />
      </div>
    </a>
    <a class="footer-nav menu">
      <div class="footer-nav-icon">
        <fa-icon :icon="['fa-solid', 'bars']" />
      </div>
    </a>
    <nuxt-link to="/" class="footer-nav home">
      <div class="footer-nav-icon">
        <fa-icon :icon="['fa-solid', 'house']" />
      </div>
    </nuxt-link>
  </footer>
</template>

<script setup lang="ts">
const router = useRouter()

const goBack = () => {
  router.back()
}
</script>

<style scoped lang="scss">
footer {
  height: 64px;
  border-top-left-radius: 24px;
  border-top-right-radius: 24px;
  background-color: #fff;
  box-shadow: 0 -2px 4px rgba(0, 0, 0, 0.3);
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  align-items: stretch;
}

.footer-nav {
  width: calc(100% / 3);
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 24px;
}

.footer-nav-icon {
  // background: linear-gradient(to right, #6cd3fb, #8b93ff);
  // -webkit-background-clip: text;
  // color: transparent;
  color: #7bb5fb;
}
</style>