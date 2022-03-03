<template>
  <nav class="cts p-y-sm">
    <div class="cts__heading">
        <img src="https://cdn2.comparethemarket.com/market/cms/logos/favicon.ico" />
        <div class="cts__heading-title">
            <h1>Compare the schema</h1>
            <p>Making rich text comparison simples!</p>
        </div>
    </div>

    <div id="cts__nav">
        <ul>
            <li>
                <a href="https://schema.org/docs/documents.html">Documentation</a>
            </li>   
            <li>
                <a href="https://schema.org/docs/schemas.html">Schemas</a>
            </li>
        </ul>
    </div>
  </nav>
</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

  .cts {
    background-color: #004183;
    color: white;
    display: flex;
    justify-content: space-evenly;

    &__heading {
        display: flex;
        
        img {
            height: 75px;
            width: 75px;
            padding: 10px;
        }
    }
  }
</style>
