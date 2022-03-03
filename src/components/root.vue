<template>
  <div>
    <Meganav />
    <div class="cntnr">
      <Form @form-submit="fetchSiteData" />
    </div>
  </div>
</template>

<script>
import Meganav from './Meganav' 
import Form from './Form' 


export default {
	name: 'HelloWorld',
	props: {
		msg: String
	},
	components: {
		Meganav,
		Form
	},
	methods: {
		fetchSiteData (evt){
			console.log(evt)
		},

		fetchSingleSite() {
			document.querySelectorAll('script[type="application/ld+json"]');
		}
	}
}
</script>

<style lang="scss" scoped>
  .header {

  }
</style>
