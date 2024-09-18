<script>
import MainCardListItem from './MainCardListItem.vue';

    export default {
        data() {
            return {
                
            }
        },
        components: {
            MainCardListItem
        }
    }
</script>

<template>
    <div class="row row-cols-lg-5 row-cols-md-3 row-cols-2 m-0">
        <div class="col gy-4" v-for="n in 20">
            <MainCardListItem/>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>



