<script>
    export default {
        data() {
            return {
                
            }
        }
    }
</script>

<template>
    <div class="loader"></div>
</template>

<style lang="scss" scoped>
    .loader {
    width: 150px;
    aspect-ratio: 1;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    animation: 
        l3-1 2s infinite linear,
        l3-2 3s infinite steps(1) -.5s;
    }
    @keyframes l3-1 {
    0%   {transform: perspective(150px) rotateX(  0deg) rotateY(0deg)}
    50%  {transform: perspective(150px) rotateX(180deg) rotateY(0deg)}
    100% {transform: perspective(150px) rotateX(180deg) rotateY(180deg)}
    }
    @keyframes l3-2 {
    0%  {background: #ff4366}
    33% {background: #ff4366}
    66% {background: #eeeeee}
    }
</style>