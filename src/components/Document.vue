<template>
  <div class="document">
    <div v-for="category in categories" :id="category.slug" class="category">
      <h3>{{ category.name }}</h3>
      <ul class="points">
        <li v-for="point in document" v-if="point.category == category.id" class="point">
          <div class="text">{{ point.text }}</div>
          <div v-if="point.status == 'DONE'" class="status status-done">
            <span class="glyphicon glyphicon-ok"></span> Fet
          </div>
          <div v-if="point.status == 'PENDING'" class="status status-pending">
            <span class="glyphicon glyphicon-time"></span> En procés
          </div>
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

<style lang="scss" scoped>
  h3 {
    font-size: 30px;
    padding: 50px 0 20px 0;
    background: linear-gradient(270deg, #D4432F, #E28333);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    display: inline-block;
  }

  .points {
    li {
      display: flex;
      align-items: center;
      font-size: 1.75rem;
      margin: 0;
      padding: 0;
      border-bottom: 1px #E1E2E3 solid;
      padding: 15px 0;
      position: relative;
      -webkit-transition: 0.2s ease-in;
    }
  }

  .text {
    padding-right: 1rem;
  }

  .status {
    flex-shrink: 0;
    flex-grow: 0;
    margin-left: auto;
    background: #DDD;
    padding: 0.5rem 2rem;
    font-size: 1.75rem;
    color: #FFF;
    white-space: nowrap;
    cursor: default;
    display: inline-block;
    width: 160px;
    text-align: center;
    position: relative;
  }

  .status-done {
    background: #26AC5B;
  }

  .status-pending {
    background: #F39B00;
  }
</style>
