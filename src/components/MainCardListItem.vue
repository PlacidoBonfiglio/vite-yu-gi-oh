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
            <p class="card-text">{{ yugiCardObject.name }}</p>
            <p class="card-text">{{ yugiCardObject.archetype }}</p>
        </div>
    </article>
</template>

<style lang="scss" scoped>
   
</style>