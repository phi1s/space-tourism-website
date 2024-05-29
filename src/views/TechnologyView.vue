<script setup lang="ts">
import { technology } from "../data";
import { ref } from 'vue'

let activeView = ref(0);

const changeActiveView = (view: number) => {
    activeView.value = view;
};

const isActive = (view: number) => {
    return activeView.value === view;
};

</script>

<template>
    <div class="technology">
        <h4><b>03</b> SPACE LAUNCH 101</h4>
        <div class="image-container">
            <img :src="technology[activeView].images.portrait" />
        </div>
        <ol>
            <li>
                <button :class="{ 'active': isActive(0) }" @click="changeActiveView(0)">1</button>
            </li>
            <li>
                <button :class="{ 'active': isActive(1) }" @click="changeActiveView(1)">2</button>
            </li>
            <li>
                <button :class="{ 'active': isActive(2) }" @click="changeActiveView(2)">3</button>
            </li>
        </ol>
        <h3>THE TERMINOLOGY…</h3>
        <h2>{{ technology[activeView].name }}</h2>
        <p>{{ technology[activeView].description }}</p>
        <div class="background" />
    </div>
</template>

<style scoped>
.background {
    background-image: url("../assets/technology/background-technology-mobile.jpg");
}

img {
    height: 100%;
    width: 100%;
    object-fit: cover;
}

.image-container {
    position: absolute;
    left: 0;
    right: 0;
    height: 300px;
    width: 100vw;
}

h4 {
    margin-bottom: 64px;
}

ol {
    width: 150px;
    margin-top: 400px;
}

li {
    border: none;
}

button {
    color: var(--color-white);
    height: 40px;
    width: 40px;
    border: 1px solid rgba(255, 255, 255, 0.5);
    background: transparent;
    border-radius: 100%;
}

.active {
    color: var(--color-very-dark-navy);
    background-color: var(--color-white);
}

@media (min-width: 1024px) {}
</style>