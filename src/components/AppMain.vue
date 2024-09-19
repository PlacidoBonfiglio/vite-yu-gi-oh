<script>
import MainCardList from './MainCardList.vue';
import MainMessage from './MainMessage.vue';
import MainSelect from './MainSelect.vue';

import {store} from '../store.js';

    export default {
        data() {
            return {
                store,
            }
        },
        components: {
            MainCardList,
            MainMessage,
            MainSelect
        }
    }
</script>

<template>
    <main>
        <section id="catalog" class="container">

            <MainSelect/>

            <div class="catalog-cards-bg">
                <MainMessage/>

                <MainCardList/>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
    div-loader {
        height: 100%;
    }

    .catalog-cards-bg {
        background-color: #212429;
        padding: 0 30px;
        border: 5px solid red;
        box-shadow: 0 0 30px red;
        border-radius: 20px;
        padding-bottom: 30px;
        margin-bottom: 80px;
    }
</style>