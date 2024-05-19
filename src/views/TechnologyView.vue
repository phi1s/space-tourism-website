<template>
    <div class="technology">
        <h4><b>03</b> SPACE LAUNCH 101</h4>
        <div class="image-container">
            <img src="../assets/technology/image-launch-vehicle-landscape.jpg" />
        </div>
        <ol>
            <li>
                <button>1</button>
            </li>
            <li>
                <button>2</button>
            </li>
            <li>
                <button>3</button>
            </li>
        </ol>
        <h3>THE TERMINOLOGY…</h3>
        <h2>LAUNCH VEHICLE</h2>
        <p>A launch vehicle or carrier rocket is a rocket-propelled vehicle used to carry a payload from Earth's surface
            to space, usually to Earth orbit or beyond. Our WEB-X carrier rocket is the most powerful in operation.
            Standing 150 metres tall, it's quite an awe-inspiring sight on the launch pad!</p>
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
    opacity: 50%;
    margin-top: 400px;
}

li {
    border: none;
}

button {
    color: var(--color-white);
    height: 40px;
    width: 40px;
    border: 1px solid var(--color-white);
    background: transparent;
    border-radius: 100%;
}

@media (min-width: 1024px) {}
</style>