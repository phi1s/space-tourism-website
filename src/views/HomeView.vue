<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter();
const goToDestination = () => { router.push('/destination'); }
</script>

<template>
  <div class="home">
    <h4>SO, YOU WANT TO TRAVEL TO</h4>
    <h1>SPACE</h1>
    <p>Let’s face it; if you want to go to space, you might as well genuinely go to outer space and not hover kind of on
      the edge of it. Well sit back, and relax because we’ll give you a truly out of this world experience!</p>
    <button @click="goToDestination">
      <h3>EXPLORE</h3>
    </button>
    <div class="background" />
  </div>
</template>


<style scoped>
button {
  width: 144px;
  height: 144px;
  margin-top: 144px;
  border: none;
  border-radius: 100%;
  cursor: pointer;
  transition: box-shadow 0.3s ease;
}

button:hover {
  box-shadow: 0 0 0 77px rgba(255, 255, 255, 0.1);
}

.background {
  background-image: url("../assets/home/background-home-mobile.jpg");
}
</style>
