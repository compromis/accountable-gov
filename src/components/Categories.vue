<template>
  <div id="categories">
    <ul>
      <li v-for="category in categories">
        <a :href="'#' + category.slug" v-smooth-scroll>{{ category.name }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'categories',

  props: {
    categories: Array
  }
}
</script>

<style lang="scss" scoped>

</style>
