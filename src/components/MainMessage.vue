<script>
import { store } from '../store.js'

    export default {
        data() {
            return {
               store 
            }
        },
    }
</script>

<template>
    <div>
        <p class="text-white fw-bold fs-3 py-3 m-0">
            Number of cards: {{ store.yugiCards.length }}
        </p>
    </div>
</template>

<style lang="scss" scoped>


</style>