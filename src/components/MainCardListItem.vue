<script>
    export default {
        data() {
            return {
                
            }
        },
        props: {
            yugiCardObject: {
                type: Object,
                required: true,
            }
        },
    }
</script>

<template>
    <article class="card p-0">
        <img :src="yugiCardObject.card_images[0].image_url" class="card-img-top" alt="...">
        <div class="card-body">
            <p class="card-text fw-bold text-center">{{ yugiCardObject.name }}</p>
            <p class="card-text text-center">{{ yugiCardObject.archetype }}</p>
        </div>
    </article>
</template>

<style lang="scss" scoped>
    .card {
        box-shadow: 0 0 8px white;

        p:first-child {
            font-size: 1.2rem;
        }
    }
</style>