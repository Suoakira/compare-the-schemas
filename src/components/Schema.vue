<template>
    <div class="accordion-item">
        <h2 class="accordion-header" id="headingOne">
        <button class="accordion-button" type="button" data-bs-toggle="collapse" :data-bs-target="'#' + schema.type" aria-expanded="false" :aria-controls="schema.type">
            {{ schema.type }}
        </button>
        </h2>
        <div :id="schema.type" class="accordion-collapse collapse" aria-labelledby="headingOne">
            <div class="accordion-body">
                <pre><code>{{ prettyPrintObj(schema) }}</code>
                </pre>
            </div>
        </div>
    </div>
</template>

<script>

export default {
	name: 'FAQ',
    props: {
        schema: Object,
    },
    methods: {
        prettyPrintObj(obj) {
            return JSON.stringify(obj,null,2)
        }
    }
}
</script>

<style lang="scss" scoped>

    .accordion-button,
    .accordion-body {
        width: 35vw;
    }

</style>
