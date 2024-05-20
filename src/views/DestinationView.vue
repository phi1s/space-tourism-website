<script setup lang="ts">
import { destinations } from "../data";
import { ref } from 'vue'

let activeView = ref(0);

const changeActiveView = (view: number) => {
    activeView.value = view;
};

</script>

<template>
    <div class="destination">
        {{ activeView }}
        <h4><b>01 </b>PICK YOUR DESTINATION</h4>
        <img src="../assets/destination/image-moon.png" />
        <ol>
            <li><button @click="changeActiveView(0)">MOON</button></li>
            <li><button @click="changeActiveView(1)">MARS</button></li>
            <li><button @click="changeActiveView(2)">EUROPA</button></li>
            <li><button @click="changeActiveView(3)">TITAN</button></li>
        </ol>
        <h1>{{ destinations[activeView].name }}</h1>
        <p>{{ destinations[activeView].description }}</p>
        <hr />
        <div class="stats-item">
            <h6>AVG. DISTANCE</h6>
            <h5>{{ destinations[activeView].distance }}</h5>
        </div>
        <div class="stats-item">
            <h6>Est. travel time</h6>
            <h5>{{ destinations[activeView].travel }}</h5>
        </div>
        <div class="background" />
    </div>
</template>

<style>
img {
    width: 150px;
    height: 150px;
}

ol {
    display: flex;
    justify-content: space-between;
    width: 250px;
    margin: auto;
    margin-top: 60px;
}

li {
    padding-bottom: 12px;
    border-bottom: 4px solid white;
}

.background {
    background-image: url("../assets/destination/background-destination-mobile.jpg");
}

@media (min-width: 1024px) {}
</style>