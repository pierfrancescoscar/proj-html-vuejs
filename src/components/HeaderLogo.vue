<template>
  <section class="container-fluid p-3">
      <div class="container">
          <div class="row">
              <div class="col-12">
                  <img class="py-4" src="../assets/logo-default-slim.png" alt="porto-logo">
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'HeaderLogo',

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';
@import '@/style/globals.scss';


section {
    background-color: $background-1;
    border-bottom: 1px solid $border-3;
}
    img {
        width: 100px;
    }

</style>