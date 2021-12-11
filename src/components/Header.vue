<template>
  <section class="container-fluid p-3">
      <div class="container">
          <div class="row">
              <div class="col-6 d-flex align-items-center w-100">
                    <nav>
                            <ul class="d-flex align-items-center mb-0 ps-0">
                                <li class="list-unstyled py-2" v-for="(link, index) in mainNavigation" :key="`link-${index}`">
                                    <a class="text-uppercase text-decoration-none me-4" :href="link.url">{{link.text}}</a>
                                </li>
                            </ul>
                    </nav>

                        <div class="col-6 d-flex justify-content-end">
                            <i class="fas fa-search"></i>
                        </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Header',
    props: {
        mainNavigation: Array,
    }
}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';
@import '@/style/globals.scss';

section {
    background-color: $background-1;
}
    a {
        color: $text-7;
        font-weight: $strong-fw;
    }

    i {
        cursor: pointer;
    }

</style>