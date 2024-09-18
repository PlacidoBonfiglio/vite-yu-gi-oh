<script>
import MainCardList from './MainCardList.vue';

    export default {
        data() {
            return {
                
            }
        },
        components: {
            MainCardList
        }
    }
</script>

<template>
    <section id="catalog" class="container">
        <div class="catalog-cards-bg">
            <div>
                <p class="text-white fw-bold fs-3 py-3 px-4 m-0">
                    Number of cards: 20
                </p>
            </div>

            <MainCardList/>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .catalog-cards-bg {
        background-color: #212429;
        border-radius: 20px;
        padding-bottom: 50px;
    }

</style>