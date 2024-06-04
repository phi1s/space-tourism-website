<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter();
const goToDestination = () => { router.push('/destination'); }
</script>

<template>
  <div class="home">
    <div class="text">
      <h4>SO, YOU WANT TO TRAVEL TO</h4>
      <h1>SPACE</h1>
      <p>Let’s face it; if you want to go to space, you might as well genuinely go to outer space and not hover kind of
        on
        the edge of it. Well sit back, and relax because we’ll give you a truly out of this world experience!</p>
    </div>
    <button @click="goToDestination">
      <h3>EXPLORE</h3>
    </button>
    <div class="background" />
  </div>
</template>


<style scoped>
h1 {
  font-size: var(--mobile-heading-XL-font-size);
  margin-top: 24px;
}

h4 {
  color: var(--color-light-blue);
}

button {
  width: 144px;
  height: 144px;
  margin-top: 112px;
  border-radius: 100%;
  color: var(--color-very-dark-navy);
  background-color: var(--color-white);
  transition: box-shadow 0.3s ease;
}

button:hover {
  box-shadow: 0 0 0 77px rgba(255, 255, 255, 0.1);
}

button>h3 {
  margin-top: 0;
}

.background {
  background-image: url("../assets/home/background-home-mobile.jpg");
}

@media (min-width: 768px) {
  button {
    width: 272px;
    height: 272px;
  }

  h4 {
    text-align: center;
  }
}

@media (min-width: 1440px) {
  .home {
    display: flex;
    justify-content: space-between;
  }

  .text {
    width: 540px;
  }

  h4 {
    text-align: start;
  }
}
</style>
