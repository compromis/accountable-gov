<template>
  <div id="categories">
    <div class="row">
      <div v-for="category in categories" :key="category.id" class="category col-sm-4 col-lg-3">
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
      border-width: 4px;
      border-style: solid;
      transition: 0.2s ease-in;

      &:hover {
        background: #FFF;
      }
    }
  }

  .category-igualtat {
    background: $igualtat;
    border-color: $igualtat;

    &:hover {
        color: $igualtat;
    }
  }
  .category-educacio-cultura {
    background: $educacio;
    border-color: $educacio;

    &:hover {
        color: $educacio;
    }
  }
  .category-sanitat {
    background: $sanitat;
    border-color: $sanitat;

    &:hover {
        color: $sanitat;
    }
  }
  .category-economia {
    background: $economia;
    border-color: $economia;

    &:hover {
        color: $economia;
    }
  }
  .category-agricultura {
    background: $agricultura;
    border-color: $agricultura;

    &:hover {
        color: $agricultura;
    }
  }
  .category-transparencia {
    background: $transparencia;
    border-color: $transparencia;

    &:hover {
        color: $transparencia;
    }
  }
  .category-habitatge {
    background: $habitatge;
    border-color: $habitatge;

    &:hover {
        color: $habitatge;
    }
  }
  .category-medi-ambient {
    background: $medi-ambient;
    border-color: $medi-ambient;

    &:hover {
        color: $medi-ambient;
    }
  }
  .category-hisenda {
    background: $hisenda;
    border-color: $hisenda;

    &:hover {
        color: $hisenda;
    }
  }
  .category-admin-publica {
    background: $admin-publica;
    border-color: $admin-publica;

    &:hover {
        color: $admin-publica;
    }
  }
  .category-justicia {
    background: $justicia;
    border-color: $justicia;

    &:hover {
        color: $justicia;
    }
  }
  .category-comunicacio {
    background: $comunicacio;
    border-color: $comunicacio;

    &:hover {
        color: $comunicacio;
    }
  }

  @media screen and (max-width: 768px) {
    .category {
      a {
        height: auto;
      }
    }
  }
</style>
