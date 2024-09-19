<script>
import MainCardListItem from './MainCardListItem.vue';
import axios from 'axios';
import MainLoader from './MainLoader.vue';

// importo store js
import {store} from '../store.js';

    export default {
        data() {
            return {
              
                // inserisco store tra i miei data
                store,
            }
        },
        components: {
            MainCardListItem,
            MainLoader
        },
    }

</script>

<template>
    <MainLoader v-if="store.yugiCards.length === 0"/>

    <div class="row row-cols-lg-6 row-cols-md-4 row-cols-3 gap-5 justify-content-center" v-else>
        <MainCardListItem v-for="yugiCard in store.yugiCards" :key="yugiCard.id" :yugiCardObject="yugiCard" />
    </div>
</template>

<style lang="scss" scoped>

</style>



