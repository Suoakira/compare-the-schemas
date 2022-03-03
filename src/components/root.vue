<template>
  <div>
    <Meganav />
		<Form @form-submit="fetchSiteData" />
	<div class="sch-cntnr">
		<SchemaContainer :rootSiteSchema="rootSiteSchema"/>
		<SchemaContainer :rootSiteSchema="comparisonSiteSchema"/>
	</div>
  </div>
</template>

<script>
import Meganav from './Meganav' 
import Form from './Form' 
import SchemaContainer from './SchemaContainer'
import ctmData  from "../assets/data-ctm"
import msmData  from "../assets/data-msm"

export default {
	name: 'rppt',
    data() {
        return {
            rootSiteSchema: null,
            comparisonSiteSchema: null,
        };
    },
	components: {
		Meganav,
		Form,
		SchemaContainer
	},
	methods: {
		// mock scrape
		fetchSiteData (evt){
			if ( evt.rootSiteInput === "https://www.comparethemarket.com/car-insurance/") {
				this.rootSiteSchema = ctmData
				}

			if ( evt.comparisonSiteOne === "https://www.moneysupermarket.com/car-insurance/") {
				this.comparisonSiteSchema = msmData
				}
			console.log(this.rootSiteSchema, this.comparisonSiteSchema)
		},
	}
}
</script>

<style lang="scss" scoped>
	.sch-cntnr {
		display: flex;
		justify-content: center;
	}	
</style>
