<script>
export default {
    data() {
        return {
            selectedArchetype: "Alien",
        }
    }
}
</script>

<template>
    <select class="form-select w-25 mb-5" aria-label="Default select example" v-model='selectedArchetype' @change="$emit('selectArchetype')">
        <option selected value="Alien">Alien</option>
        <option value="Anfernoble Arms">Infernoble Arms</option>
        <option value="Noble Knight">Noble Knight</option>
        <option value="Melodious">Melodious</option>
        <option value="Archfiend">Archfiend</option>
    </select>
</template>

<style lang="scss">

</style>