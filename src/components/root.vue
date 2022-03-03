<template>
  <div>
    <Meganav />
    <div class="cntnr">
      <Form @form-submit="fetchSiteData" />
    </div>
	<FaQContainer :rootSiteSchema="rootSiteSchema"/>
  </div>
</template>

<script>
import Meganav from './Meganav' 
import Form from './Form' 
import FaQContainer from './FaQContainer'
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
		FaQContainer
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
  .header {

  }
</style>
