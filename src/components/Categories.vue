<template>
  <section class="container-fluid p-5">
      <div class="container d-flex justify-content-center">
          <div class="row w-100">
              <div class="col-12 d-flex w-100">

                  <nav class="w-100">
                      
                      <ul class="ps-0 d-flex justify-content-between align-items-center mb-0">

                          <i class="fas fa-chevron-left"></i>

                            <Tag v-for="(category, index) in categories" :key="`category-${index}`"
                            :title="category.text"
                            :url="category.url"
                            />

                            <i class="fas fa-chevron-right"></i>

                      </ul>
                  </nav>

              </div>
          </div>
      </div>
  </section>
</template>

<script>
import Tag from '@/components/Tag.vue';

export default {
    name: 'Categories',
    components: {
        Tag,
    },
    props: {
        categories: Array,
    }

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';

section {
    background-color: $background-4;
}
    i {
        cursor: pointer;
        color: $border-9;
    }

</style>