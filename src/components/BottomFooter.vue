<template>
  <section class="container-fluid p-4">
      <div class="container">
          <div class="row align-items-center">

              <div class="col-6">
                  <img class="me-5" src="../assets/logo-footer.png" alt="porto-logo">
                    <span class="ps-5 copyright">
                        &copy;
                        Copyright 2020. All Rights Reserved. 
                    </span>
              </div>

              <div class="col-6">

                <div class="breadcrumbs">
                    <span class="pe-2">
                        <i class="pe-2 fas fa-chevron-right"></i>
                        FAQ's
                    </span>

                    <span class="pe-2">
                        <i class="pe-2 fas fa-chevron-right"></i>
                        Sitemap
                    </span>

                    <span class="pe-2">
                        <i class="pe-2 fas fa-chevron-right"></i>
                        Contact us
                    </span>
                  </div>

              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'BottomFooter'

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';
@import '@/style/globals.scss';


section {
    background-color: $background-9;
}
    img {
        width: 80px;
    }

    .copyright {
        font-size: $minor-fs;
        color: $text-6;
    }

    span {
        font-size: $minor-fs;
        color: $text-6;
        cursor: pointer;
    }

    .breadcrumbs {
        text-align: right;
    }

</style>