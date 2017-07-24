<template>
  <div id="document">
    <div v-for="category in categories" :id="category.slug">
      <h3>{{ category.name }}</h3>
      <ul>
        <li v-for="point in document" v-if="point.category == category.id">
          {{ point.text }}
          {{ point.status }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'document',

  props: {
    document: Array,
    categories: Array,
  },
}
</script>

<style lang="scss">

</style>
