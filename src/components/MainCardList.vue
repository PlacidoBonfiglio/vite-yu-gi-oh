<script>
import MainCardListItem from './MainCardListItem.vue';
import axios from 'axios';

    export default {
        data() {
            return {
              yugiCards: [],
              apiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0'  
            }
        },

        methods: {
            //Chiamo Api con un metodo
            getYugiCards() {
                axios.get(this.apiUrl)
                // Per sovrascrivere un dato e usare il this ho bisogno di un arrow function 
                .then((response) => {
                    console.log(response.data.data);
                    this.yugiCards = response.data.data;
                })
                .catch(function (error) {
                    console.log(error);
                });
            }
        },

        components: {
            MainCardListItem
        },

        // Creo un hook per chiamare il metodo
        mounted() {
            this.getYugiCards()
        }
    }

</script>

<template>
    <div class="">
        <div class="row row-cols-lg-6 row-cols-md-4 row-cols-3 gap-5 justify-content-center">
            <MainCardListItem v-for="yugiCard in yugiCards" :key="yugiCard.id" :yugiCardObject="yugiCard" />
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>



