<template>
    <div class="mb-3 cts__form">
        <label for="exampleFormControlInput1" class="form-label">Page url of which you wish to compare</label>
        <input type="text" class="form-control" v-model="rootSiteInput" >

        <label class="form-label cts__form-2">Page's you wish to compare to</label>
        <input type="text" class="form-control cts__form-input" v-model="comparisonSiteOne">
        <button @click="formSubmit"> Submit </button>
    </div>
</template>

<script>

export default {
    name: 'Form',
    data() {
        return {
            rootSiteInput: "url of site you wish to compare",
            comparisonSiteOne: "url of site you want to compare to",
        };
    },
    methods: {
        formSubmit (){

            const formObj = {
                rootSiteInput: this.rootSiteInput,
                comparisonSiteOne: this.comparisonSiteOne
            }

            this.$emit('form-submit', formObj)
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

    .cts {
        &__form {
            padding: 20px 0px;

            &-2 {
                padding-top: 20px;
            }

            &-input {
                margin: 5px 0px;
            }
        }
    }

</style>
