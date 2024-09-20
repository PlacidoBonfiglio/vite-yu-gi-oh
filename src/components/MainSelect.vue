<script>
import axios from 'axios';

export default {
    data() {
        return {
            archetypesList: [],
            selectedItem: '',
            apiArchetypeUrl: 'https://db.ygoprodeck.com/api/v7/archetypes.php',
        }
    },

    methods: {
        getArchetype(message) {
            this.$emit('actualArchetype', message);
            //console.log(value)
        },

        getAllArchetypes() {
            axios.get(this.apiArchetypeUrl)
            
            .then((response) => {
                console.log(response.data);
                this.archetypesList = response.data;
            })
            .catch(function (error) {
                console.log(error);
            });
        },
    },
    created() {
        this.getAllArchetypes();
    }

}
</script>

<template>
    <select class="form-select w-25 mb-5" v-model='selectedItem' @change="getArchetype(selectedItem)">
        <option v-for="(archetype, index) in archetypesList" :key="index" value="archetype.archetype_name">{{ archetype.archetype_name }}</option>
    </select>
</template>

<style lang="scss">

</style>