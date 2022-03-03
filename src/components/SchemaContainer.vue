<template>
    <div class="accordion" id="accordionExample" v-if="rootSiteSchema != null">
        <div v-for="schema in rootSiteSchema" :key="schema.type">
            <Schema  :schema="schema"  />
        </div>
    </div>
</template>

<script>
import Schema from './Schema' 

export default {
	name: 'SchemaContainer',
    props: {
        rootSiteSchema: Array,
    },
    components: {
        Schema
    }
}
</script>

<style lang="scss" scoped>

</style>
