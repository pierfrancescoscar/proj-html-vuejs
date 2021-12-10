<template>
  <section class="container-fluid p-5">
      <section class="container">
          <div class="row">
              <div class="col-3">
                  <h3 class="text-white text-uppercase">About the Blog</h3>
                  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor, sit amet.</p>
                  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores eligendi cumque suscipit accusantium...</p>
                  <h3 class="text-white text-uppercase view-more">View more
                      <i class="fas fa-chevron-right"></i>
                  </h3>
              </div>
              <div class="col-3">
                  <h3 class="text-white text-uppercase">Recent Posts</h3>
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
     h3 {
        color: $text-7;
        font-weight: $strong-fw;
        font-size: $medium-fs;

    }

    p {
        font-size: $minor-fs;
        color: $text-5;
    }

    i {
        font-size: $minor-fs;
    }

    .view-more {
        cursor: pointer;
    }
</style>