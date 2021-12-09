<template>
  <section class="container-fluid p-5">
      <div class="container">
          <div class="row">
              <div class="col-12">
                  <nav>
                      <ul class="d-flex flex-wrap ps-0">
                          <li class="list-unstyled pe-4" v-for="(post, index) in articles" :key="`article-${index}`">
                              <div>
                                  <img class="img-fluid" :src="require(`@/assets/${post.image}.jpg`)" :alt="post.text">

                                    <div class="post-content w-100">
                                        <div class="category-tag pb-3">
                                            <span class="text-white text-uppercase p-2 rounded">
                                                {{post.category}}
                                            </span>
                                        </div>
                                        <div class="post-title w-100">
                                            <a class="text-decoration-none text-white" :href="post.url">{{post.text}}</a>
                                        </div>
                                    </div>
                              </div>
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
        position: relative;
    
    }

    span {
        font-weight: $medium-fw;
        font-size: $minor-fs;
        background-color: $background-4;
    }

    a {
        font-size: $medium-fs;
        font-weight: $extrastrong-fw;
    }

    li:nth-child(1), li:nth-child(2), li:nth-child(3) {
        margin-bottom: 1.5rem;
    }

    .post-content { 
        position: absolute;
        bottom: 20px;
        left: 20px;
    }
        
    
</style>