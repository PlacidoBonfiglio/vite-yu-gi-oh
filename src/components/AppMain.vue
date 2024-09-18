<script>
import MainCardList from './MainCardList.vue';
import MainMessage from './MainMessage.vue';

    export default {
        data() {
            return {
                
            }
        },
        components: {
            MainCardList,
            MainMessage
        }
    }
</script>

<template>
    <section id="catalog" class="container">
        <div class="catalog-cards-bg">
            <MainMessage/>

            <MainCardList/>
        </div>
    </section>
</template>

<style lang="scss" scoped>
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