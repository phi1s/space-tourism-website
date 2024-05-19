<template>
    <div class="crew">
        <h4><b>02</b> MEET YOUR CREW</h4>
        <h3>COMMANDER</h3>
        <h2>Douglas Hurley</h2>
        <p>Douglas Gerald Hurley is an American engineer, former Marine Corps pilot and former NASA astronaut. He
            launched into space for the third time as commander of Crew Dragon Demo-2.</p>
        <ol>
            <li>
                <div class="dot" />
            </li>
            <li>
                <div class="dot" />
            </li>
            <li>
                <div class="dot" />
            </li>
            <li>
                <div class="dot" />
            </li>
        </ol>
        <img src="../assets/crew/image-douglas-hurley.png" />
        <div class="background" />
    </div>
</template>

<style scoped>
h3 {
    margin-top: 64px;
}

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
    opacity: 50%;
}

li {
    border: none;
}

.dot {
    width: 10px;
    height: 10px;
    background-color: var(--color-white);
    border-radius: 100%;
}

@media (min-width: 1024px) {}
</style>