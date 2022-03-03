<template>
    <div class="accordion" id="accordionExample" v-if="rootSiteSchema != null">
        <div v-for="schema in rootSiteSchema" :key="schema.type">
            <FaQ  :schema="schema"  />
        </div>
    </div>
</template>

<script>
import FaQ from './FaQ' 

export default {
	name: 'FAQ',
    props: {
        rootSiteSchema: Array,
    },
    components: {
        FaQ
    }
}
</script>

<style lang="scss" scoped>

</style>
