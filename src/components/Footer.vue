<template>
  <section class="container-fluid p-5">
      <section class="container">
          <div class="row">
              <div class="col-3 about">
                  <img class="getintouch" src="../assets/porto_getintouch-01.png" alt="get-in-touch">
                  <h3 class="text-white text-uppercase pb-3">About the Blog</h3>
                  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor, sit amet.</p>
                  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores eligendi cumque suscipit accusantium...</p>
                  <h3 class="text-white text-uppercase view-more">View more
                      <i class="fas fa-chevron-right"></i>
                  </h3>
              </div>
              <div class="col-3">
                  <h3 class="text-white text-uppercase pb-3">Recent Posts</h3>
                    <nav>
                            <ul class="ps-0">
                                <li class="list-unstyled pe-2" v-for="(element, index) in recentPosts" :key="`post-${index}`">

                                    <div class="d-flex pt-2">

                                        <div class="pe-3">
                                            <img class="rounded-circle" :src="require(`@/assets/${element.image}.jpg`)" alt="recent-post-feed">
                                        </div>

                                        <div class="d-flex flex-column">

                                            <a class="text-decoration-none" :href="element.url">
                                                {{element.text}}
                                            </a>

                                            <span>
                                                {{element.date}}
                                            </span>
                                        </div>

                                    </div>

                                </li>
                            </ul>
                    </nav>
              </div>
              <div class="col-3">
                  <h3 class="text-white text-uppercase pb-3">Recent Comments</h3>
                  <nav>
                      <ul class="ps-0">
                          <li class="list-unstyled">
                              <a class="text-decoration-none" href="#">
                                  <i class="blue-arrow fas fa-chevron-right pe-2"></i>
                                  <strong>John Doe</strong> commented on <strong>
                                      <span class="blue-link">
                                          lorem ipsum dolor sit amet.
                                      </span>
                                      </strong>
                              </a>

                              <div class="date">
                                <span>12:55 AM Dec 19th</span>
                              </div>

                          </li>

                          <li>

                              <a class="text-decoration-none" href="#">
                                  <i class="blue-arrow fas fa-chevron-right pe-2"></i>
                                  <strong>John Doe</strong> commented on 
                                  <strong>
                                    <span class="blue-link">lorem ipsum dolor sit amet.
                                    </span>
                                        </strong>
                              </a>

                              <div class="date">
                                <span>12:55 AM Dec 19th</span>
                              </div>

                          </li>
                      </ul>
                  </nav>
              </div>
              <div class="col-3">

                <h3 class="text-white text-uppercase pb-3">Categories</h3>

                    <nav>
                        <ul class="ps-0 d-flex flex-wrap">
                            <li class="list-unstyled me-2 mb-4" v-for="(element, index) in footerCategories" :key="`category-${index}`">
                                <a class="footer-categories text-uppercase text-decoration-none rounded p-2" :href="element.url">
                                    {{element.text}}
                                </a>
                            </li>
                        </ul>
                    </nav>
              </div>
          </div>
      </section>
  </section>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        recentPosts: Array,
        footerCategories: Array,
    }

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';
@import '@/style/globals.scss';


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

    a {
        color: $text-2;
        font-size: $minor-fs;
    }

    i {
        font-size: $minor-fs;
    }

    span {
        color: $text-5;
        font-size: $minor-fs;
    }

    img {
        width: 50px;
        height: 50px;
    }

    .view-more {
        cursor: pointer;
    }

    .blue-link, .blue-arrow  {
        color: $text-4;
    }

    .footer-categories {
        color: $text-1;
        font-size: $minor-fs;
        font-weight: $strong-fw;
        background-color: $background-12;

    }

    .about {
        position: relative;
    }

    .getintouch {
        object-fit: contain;
        width: 150px;
        height: 80px;
        position: absolute;
        top: -106px;
    }
</style>