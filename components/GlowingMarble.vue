<template>
    <ball><slot></slot></ball>
</template>

<style scoped>
body {
  background-color: transparent;
}

ball {
    opacity: 0.3;
    position: absolute;
    left: 44.1%;
    top: 60%;
    width: 300px;
    height: 300px;
    border-radius: 50%;
    box-shadow:
        inset 0 0 50px #00E676,
        inset 20px 0 80px #FFFFFF,
        inset -20px 0 80px #76FF03,
        inset 20px 0 300px white,
        inset -20px 0 300px greenyellow,
        0 0 50px #fff,
        -10px 0 80px #76FF03,
        10px 0 80px #76FF03;
}

ball:hover {
    transition: .5s;
    opacity: 1;
    box-shadow:
    inset 0 0 50px #00E676,
        inset 20px 0 160px #FFFFFF,
        inset -30px 0 160px #76FF03,
        inset 20px 0 500px white,
        inset -30px 0 500px greenyellow,
        0 0 50px #fff,
        -16px 0 160px #76FF03,
        10px 0 160px #76FF03;
}

ball:not(:hover) {
    transition: .5s;
    opacity: 0.3;
    position: absolute;
    left: 44.1%;
    top: 60%;
    width: 300px;
    height: 300px;
    border-radius: 50%;
    box-shadow:
        inset 0 0 50px #00E676,
        inset 20px 0 80px #FFFFFF,
        inset -20px 0 80px #76FF03,
        inset 20px 0 300px white,
        inset -20px 0 300px greenyellow,
        0 0 50px #fff,
        -10px 0 80px #76FF03,
        10px 0 80px #76FF03;    
}

</style>

<script setup>
function shakeBall() {
    console.log('smart mf');
}
</script>