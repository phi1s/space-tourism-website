<script setup lang="ts">
import { ref } from 'vue'

const isOverlay = ref(false)

const toggleNav = () => {
  isOverlay.value = !isOverlay.value;
};
</script>

<template>
  <header>
    <div class="menu">
      <RouterLink to="/">
        <img id="logo" src="./assets/shared/logo.svg" />
      </RouterLink>
      <button @click="toggleNav" class="hamburger">
        <img id="hamburger" src="./assets/shared/icon-hamburger.svg" />
      </button>
    </div>
    <div v-if="isOverlay" class="mobile-nav">
      <button @click="toggleNav">
        <img id="close" src="./assets/shared/icon-close.svg" />
      </button>
      <nav>
        <RouterLink to="/" class="link" activeClass="active" @click="toggleNav"><b>00</b>Home</RouterLink>
        <RouterLink to="/destination" class="link" activeClass="active" @click="toggleNav"><b>01</b>Destination
        </RouterLink>
        <RouterLink to="/crew" class="link" activeClass="active" @click="toggleNav"><b>02</b>Crew</RouterLink>
        <RouterLink to="/technology" class="link" activeClass="active" @click="toggleNav"><b>03</b>Technology
        </RouterLink>
      </nav>
    </div>
  </header>
  <main>
    <RouterView />
  </main>
</template>

<style scoped>
.mobile-nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: 100;
  background-color: var(--color-very-dark-navy);
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
  top: 36px;
  right: 40px;
  height: 19px;
  width: 19px;
  margin-top: 8px;
}

.menu {
  display: flex;
  justify-content: space-between;
  margin-bottom: 24px;
}

nav {
  width: 222px;
  margin: auto;
  margin-top: 133px;
  color: var(--color-white)
}

.link {
  display: block;
  width: 100%;
  margin-bottom: 24px;
  text-align: start;
  color: inherit;
  text-decoration: none;
}

.link>b {
  opacity: 100%;
}

.active {
  border: none;
  border-right: 3px solid var(--color-white);
}

@media (min-width: 768px) {
  .hamburger {
    display: none;
  }
}
</style>
