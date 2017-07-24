<template>
  <div>
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

</style>
