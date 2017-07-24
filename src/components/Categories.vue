<template>
  <div id="categories">
    <div class="row">
      <div v-for="category in categories" class="category col-sm-3">
        <a :href="'#' + category.slug" :class="'category-' + category.slug" v-smooth-scroll>
          {{ category.name }}
        </a>
      </div>
    </div>
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

  /* Category colors */
  $igualtat:      #e28026;
  $educacio:      #e07b26;
  $sanitat:       #df7626;
  $economia:      #de7026;
  $agricultura:   #dd6a26;
  $transparencia: #dc6526;
  $habitatge:     #db6027;
  $medi-ambient:  #d95a27;
  $hisenda:       #d85527;
  $admin-publica: #d74e27;
  $justicia:      #d64a27;
  $comunicacio:   #d54427;

  .category {
    margin-bottom: 2.5rem;

    a {
      display: block;
      height: 15rem;
      padding: 2rem;
      font-family: 'Compromis', sans-serif;
      font-size: 2rem;
      color: #FFF;

      &:hover {
        opacity: 0.8;
      }
    }
  }

  .category-igualtat {
    background: $igualtat;
  }
  .category-educacio-cultura {
    background: $educacio;
  }
  .category-sanitat {
    background: $sanitat;
  }
  .category-economia {
    background: $economia;
  }
  .category-agricultura {
    background: $agricultura;
  }
  .category-transparencia {
    background: $transparencia;
  }
  .category-habitatge {
    background: $habitatge;
  }
  .category-medi-ambient {
    background: $medi-ambient;
  }
  .category-hisenda {
    background: $hisenda;
  }
  .category-admin-publica {
    background: $admin-publica;
  }
  .category-justicia {
    background: $justicia;
  }
  .category-comunicacio {
    background: $comunicacio;
  }
</style>
