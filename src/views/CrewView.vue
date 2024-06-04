<script setup lang="ts">
import { crew } from "../data";
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
    <div class="crew">
        <div class="container">
            <div class="item">
                <h4><b>02</b> MEET YOUR CREW</h4>
                <h3>{{ crew[activeView].role }}</h3>
                <h2>{{ crew[activeView].name }}</h2>
                <p>{{ crew[activeView].bio }}</p>
                <ol>
                    <li>
                        <div class="dot" :class="{ 'active': isActive(0) }" @click="changeActiveView(0)" />
                    </li>
                    <li>
                        <div class="dot" :class="{ 'active': isActive(1) }" @click="changeActiveView(1)" />
                    </li>
                    <li>
                        <div class="dot" :class="{ 'active': isActive(2) }" @click="changeActiveView(2)" />
                    </li>
                    <li>
                        <div class="dot" :class="{ 'active': isActive(3) }" @click="changeActiveView(3)" />
                    </li>
                </ol>
            </div>
            <div class="item"> <img :src="crew[activeView].images.png" /></div>
        </div>

        <div class="background" />
    </div>
</template>

<style scoped>
.background {
    background-image: url("../assets/crew/background-crew-mobile.jpg");
}

img {
    width: 270px;
    height: auto;
    margin-top: 40px;
}

ol {
    width: 100px;
    display: flex;
    margin: auto;

}

li {
    border: none;
    cursor: pointer;
    padding: 6px;
}

p {
    height: 164px;
}

h3 {
    margin-top: 200px;
}

.dot {
    width: 10px;
    height: 10px;
    background-color: var(--color-white);
    border-radius: 100%;
    opacity: 50%;
    border: none;
}

.active {
    opacity: 100%;
}

@media (min-width: 768px) {
    img {
        width: 446px;
    }
}

@media (min-width: 1440px) {
    .container {
        display: flex;
        justify-content: space-between;
    }

    .item {
        width: 50%;
    }

    ol {
        margin-left: 0;

    }

    img {
        width: 100%;
        margin-left: 32px;
    }
}
</style>