<template>
  <div>
    <div class="header">
      <h2><img src="./assets/logo.png" alt="Un govern que compleix" /></h2>
    </div>
    <categories :categories="categories" />
    <hr />
    <document :categories="categories" :document="document" />
  </div>
</template>

<script>
import Categories from './components/Categories.vue'
import Document from './components/Document.vue'

import data from './data/data.val.json'

export default {
  name: 'app',

  components: {
    Categories,
    Document
  },

  data() {
    return {
      document: [],
      categories: []
    }
  },

  mounted() {
    this.document = data.document
    this.categories = data.categories
  }
}
</script>

<style lang="scss">
  .header {
    text-align: center;
    font-size: 3.5rem;
    margin: 2rem 0 5rem;
    padding: 0 3rem;

    img {
      width: 100%;
    }
  }

  .header-page {
    h1 {
      display: none;
    }
  }

  .page-nav {
    margin-bottom: 10px;
  }
</style>
