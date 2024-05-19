<template>
    <div class="destination">
        <h4><b>01 </b>PICK YOUR DESTINATION</h4>
        <img src="../assets/destination/image-moon.png" />
        <ol>
            <li>MOON</li>
            <li>MARS</li>
            <li>EUROPA</li>
            <li>TITAN</li>
        </ol>
        <h1>MOON</h1>
        <p>See our planet as you’ve never seen it before. A perfect relaxing trip away to help regain perspective and
            come back refreshed. While you’re there, take in some history by visiting the Luna 2 and Apollo 11 landing
            sites.</p>
        <hr />
        <div class="stats-item">
            <h6>AVG. DISTANCE</h6>
            <h5>384,400 km</h5>
        </div>
        <div class="stats-item">
            <h6>Est. travel time</h6>
            <h5>3 days</h5>
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