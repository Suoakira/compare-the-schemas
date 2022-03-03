<template>
  <Meganav />
</template>

<script>
import Meganav from './Meganav' 

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    Meganav
  }
}
</script>

<style lang="scss" scoped>
  .header {

  }
</style>
