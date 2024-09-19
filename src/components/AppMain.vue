<script>
import axios from 'axios';
import MainCardList from './MainCardList.vue';
import MainMessage from './MainMessage.vue';
import MainSelect from './MainSelect.vue';

import {store} from '../store.js';

    export default {
        data() {
            return {
                store,
                //yugiCards: [],
                apiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php/',
            }
        },
        components: {
            MainCardList,
            MainMessage,
            MainSelect
        },
        methods: {
            //Chiamo Api con un metodo
            getYugiCards() {
                axios.get(this.apiUrl, {
                    params: {
                        num: 20,
                        offset: 0,
                        archetype: 'alien'
                    }
                })
                // Per sovrascrivere un dato e usare il this ho bisogno di un arrow function 
                .then((response) => {
                    console.log(response.data.data);
                    store.yugiCards = response.data.data;
                })
                .catch(function (error) {
                    console.log(error);
                });
            },

            // Metodo archetypes
            getNewArchetype(archetypeValue) {
                console.log(archetypeValue)
            },
        },
        

        // Creo un hook per chiamare il metodo
        mounted() {
            setTimeout(this.getYugiCards, 3000)
        }
    }
</script>

<template>
    <main>
        <section id="catalog" class="container">

            <MainSelect @actualArchetype="getNewArchetype"/>

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