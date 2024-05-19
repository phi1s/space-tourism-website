<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/destination">Destination</RouterLink>
      <RouterLink to="/crew">Crew</RouterLink>
      <RouterLink to="/technology">Technology</RouterLink>
    </nav>
  </header>
  <main>
    <RouterView />
  </main>
</template>

<style scoped></style>
