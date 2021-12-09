<template>
  <section class="container-fluid p-5">
      <div class="container">
          <div class="row">
              <div class="col-12">
                  <nav>
                      <ul class="d-flex flex-wrap ps-0">
                          <li class="list-unstyled pe-4" v-for="(post, index) in articles" :key="`article-${index}`">
                                  <img class="img-fluid" :src="require(`@/assets/${post.image}.jpg`)" :alt="post.text">
                                  <a :href="post.url">{{post.text}}</a>
                                  <span>test</span>
                          </li>
                      </ul>
                  </nav>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'MainArticles',
    props: {
        articles: Array,
    }

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';

section {
    background-color: $background-2;
}

    li {
        width: calc(100% / 3);
    
    }
    

</style>