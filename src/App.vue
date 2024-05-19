<script setup lang="ts">
import { ref } from 'vue'

const isOverlay = ref(false)

const toggleNav = () => {
  isOverlay.value = !isOverlay.value;
};
</script>

<template>
  <header>
    <div class="mobile-header">
      <RouterLink to="/">
        <img id="logo" src="./assets/shared/logo.svg" />
      </RouterLink>
      <button @click="toggleNav">
        <img id="hamburger" src="./assets/shared/icon-hamburger.svg" />
      </button>
    </div>
    <div v-if="isOverlay" class="mobile-nav">
      <button @click="toggleNav">
        <img id="close" src="./assets/shared/icon-close.svg" />
      </button>
      <nav>
        <RouterLink to="/" class="link" @click="toggleNav"><b>00</b>Home</RouterLink>
        <RouterLink to="/destination" class="link" @click="toggleNav"><b>01</b>Destination</RouterLink>
        <RouterLink to="/crew" class="link" @click="toggleNav"><b>02</b>Crew</RouterLink>
        <RouterLink to="/technology" class="link" @click="toggleNav"><b>03</b>Technology</RouterLink>
      </nav>
    </div>
  </header>
  <main>
    <RouterView />
  </main>
</template>

<style scoped>
.mobile-nav {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: 100;
  background-color: var(--color-very-dark-navy);
}

button {
  background-color: transparent;
  border: none;
}

#logo {
  height: 40px;
  width: 40px;
}

#hamburger {
  height: 21px;
  width: 24px;
  margin-top: -8px;
}

#close {
  position: absolute;
  top: 48px;
  right: 48px;
  height: 19px;
  width: 19px;
  margin-top: 8px;
}

.mobile-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 56px;
}

nav {
  display: flex;
  flex-direction: column;
  margin-top: 200px;
  margin-left: 40px;
  align-items: flex-start;
}

.link {
  margin-bottom: 24px;
  color: inherit;
  text-decoration: none;
}
</style>
