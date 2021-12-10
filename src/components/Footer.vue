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
                  <h3 class="text-white text-uppercase">Recent Comments</h3>
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
    props: {
        recentPosts: Array,
    }

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
</style>