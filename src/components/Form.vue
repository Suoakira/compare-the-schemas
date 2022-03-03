<template>
    <div>
    <div class="mb-3 cts__form">
        <div class="cts__form-i">
            <label for="exampleFormControlInput1" class="form-label">Page url</label>
            <input type="text" class="form-control" v-model="rootSiteInput" >
        </div>
        <div class="cts__form-i"> 
            <label class="form-label cts__form-2">Comparison page url</label>
            <input type="text" class="form-control cts__form-input" v-model="comparisonSiteOne">
        </div>
    </div>
        <button class="btn btn--dsc" @click="formSubmit"> Compare </button>
    </div>
</template>

<script>
export default {
    name: 'Form',
    data() {
        return {
            rootSiteInput: "",
            comparisonSiteOne: "",
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
            margin: 0 auto;
            text-align: center;

            &-2 {
                padding-top: 20px;
            }

            &-input {
                margin: 5px 0px;
            }

            &-i {
                display: inline-block;
                width: 35vw;
            }
        }
    }

    button {
        margin-bottom: 40px;
        left: 50%;
        position: relative;
        transform: translateX(-50%);
    }

</style>
