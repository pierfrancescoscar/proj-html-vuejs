<template>
  <section class="container-fluid p-5">
      <section class="container">
          <div class="row">
              <div class="col-3">
                  Footer 1
              </div>
              <div class="col-3">
                  Footer 2
              </div>
              <div class="col-3">
                  Footer 3
              </div>
              <div class="col-3">
                  Footer 4
              </div>
              <div class="col-3">
                  Footer 5
              </div>
          </div>
      </section>
  </section>
</template>

<script>
export default {
    name: 'Footer',

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';

section {
    background-color: $background-8;
}

</style>