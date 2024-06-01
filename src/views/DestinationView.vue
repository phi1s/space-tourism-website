<script setup lang="ts">
import { destinations } from "../data";
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
    <div class="destination">
        <h4><b>01 </b>PICK YOUR DESTINATION</h4>
        <div class="container">
            <div class="item">

                <img :src="destinations[activeView].images.png" />
            </div>
            <div class="item">
                <ol>
                    <li :class="{ 'active': isActive(0) }"><button @click="changeActiveView(0)">MOON</button></li>
                    <li :class="{ 'active': isActive(1) }"><button @click="changeActiveView(1)">MARS</button></li>
                    <li :class="{ 'active': isActive(2) }"><button @click="changeActiveView(2)">EUROPA</button></li>
                    <li :class="{ 'active': isActive(3) }"><button @click="changeActiveView(3)">TITAN</button></li>
                </ol>
                <h1>{{ destinations[activeView].name }}</h1>
                <p>{{ destinations[activeView].description }}</p>
                <hr />
                <div class="stats-container">
                    <div class="stats-item">
                        <h6>AVG. DISTANCE</h6>
                        <h5>{{ destinations[activeView].distance }}</h5>
                    </div>
                    <div class="stats-item">
                        <h6>Est. travel time</h6>
                        <h5>{{ destinations[activeView].travel }}</h5>
                    </div>
                </div>
            </div>
        </div>
        <div class="background" />
    </div>
</template>

<style>
h4 {
    margin-bottom: 32px;
}

img {
    width: 150px;
    height: 150px;
}

ol {
    display: flex;
    justify-content: space-between;
    width: 250px;
    margin: auto;
    margin-top: 32px;
}

li {
    color: var(--color-light-blue);
    padding-bottom: 12px;
}

button {
    color: inherit;
}

.active {
    color: var(--color-white);
    border-bottom: 4px solid var(--color-white);
}

.background {
    background-image: url("../assets/destination/background-destination-mobile.jpg");
}


@media (min-width: 768px) {
    .stats-container {
        display: flex;
        justify-content: space-around;
    }

    img {
        width: 300px;
        height: 300px;
    }
}


@media (min-width: 1440px) {
    .container {
        display: flex;
        justify-content: space-between;
    }

    .item,
    .stats-item {
        width: 50%;
    }

    ol {
        margin-left: 0;
    }

    img {
        width: 480px;
        height: 480px;
    }
}
</style>