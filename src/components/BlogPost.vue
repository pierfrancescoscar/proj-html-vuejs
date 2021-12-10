<template>
  <section class="container-fluid p-5">
      <div class="container">
          <div class="row">
              <div class="col-8">
                  <nav>
                      <ul class="ps-0">

                        <SingleBlogPost v-for="(post, index) in blogPost" :key="`post-${index}`"
                        :image="post.image"
                        :title="post.title"
                        :description="post.description"
                        :dateNumber="post.dateNumber"
                        :dateMonth="post.dateMonth"
                        :author="post.author"
                        :category="post.category"
                        :comments="post.comments"
                        :multipleImages="post.multipleImages"
                        />
                            
                      </ul>
                  </nav>

                  <div class="select-page d-flex justify-content-end">
                      <div class="numbered-pages rounded">
                          <span class="select icon">
                              <i class="arrow-icon fas fa-chevron-left"></i>
                          </span>
                          <span class="select one">
                              1
                          </span>
                          <span class="select two">
                              2
                          </span>
                          <span class="select three">
                              3
                          </span>
                          <span class="select icon-2">
                              <i class="arrow-icon fas fa-chevron-right"></i>
                          </span>
                      </div>
                  </div>
              </div>
              <div class="col-4">
                  <h3 class="text-uppercase pb-2">Latest from Twitter</h3>

                  <div class="tweets-container d-flex">

                        <div class="twitter-icon pe-3">
                            <i class="fab fa-twitter"></i>
                        </div>

                        <div class="tweets-text d-flex flex-column">

                            <span class="tweet">
                                If you have any suggestions for the next updates, let us know.
                            </span>

                            <span class="tweet-date">
                                01:05 PM Sep 18th
                            </span>
                        </div>

                  </div>

                  <div class="tweets-container d-flex pt-4 pb-5">

                        <div class="twitter-icon pe-3">
                            <i class="fab fa-twitter"></i>
                        </div>

                        <div class="tweets-text d-flex flex-column">

                            <span class="tweet">
                                We have just update Porto Admin. Check the changelog for more information.
                            </span>

                            <span class="tweet-date">
                                01:04 PM Sep 18th
                            </span>
                        </div>

                  </div>

                    <h3 class="text-uppercase pb-3">Photos from Instagram</h3>

                    <div class="instagram-content d-flex flex-wrap">
                    
                        <div class="instagram-feed"
                        v-for="(element, index) in instaPost" :key="`igfeed-${index}`">

                            <img class="img-fluid" :src="require(`@/assets/${element}.jpg`)" alt="insta-feed">

                        </div>

                    </div>

                    <h3 class="text-uppercase py-4">Tags</h3>

                        <nav>
                            <ul class="d-flex ps-0">
                                <li class="list-unstyled pe-2" v-for="(element, index) in instaTags" :key="`tag-${index}`">
                                    <a class="text-decoration-none text-uppercase px-2 py-1 rounded-pill" :href="element.url">{{element.text}}</a>
                                </li>
                            </ul>
                        </nav>

                    <h3 class="text-uppercase pt-5">Find us on Facebook</h3>

                    <div class="d-flex pt-4 pb-5 align-items-center">

                        <div class="custom-separator">
                            
                        </div>

                        <div class="d-flex flex-column">

                            <span class="ps-3 okler-themes">
                                Okler Themes
                            </span>

                        </div>

                  </div>

              </div>
          </div>
      </div>
  </section>
</template>

<script>
import SingleBlogPost from '@/components/SingleBlogPost.vue';

export default {
    name: 'BlogPost',
    components: {
        SingleBlogPost,
    },

    props: {
        blogPost: Array,
        instaPost: Array,
        instaTags: Array,
    }

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';

section {
    background-color: $background-1;
}

     h3 {
        color: $text-7;
        font-weight: $strong-fw;
        font-size: $medium-fs;

    }

    i {
        font-size: $big-fs;
    }

    a {
        color: $text-1;
        font-size: $minor-fs;
        background-color: $background-7;
        font-weight: $strong-fw;
    }

    .tweet {
        color: $text-3;
        font-size: $medium-fs;
    }

    .tweet-date {
        color: $text-4;
        font-size: $minor-fs;
    }

    .instagram-feed {
        width: calc(100% / 3);
    }

    .instagram-content {
        cursor: pointer;
    }

    .custom-separator {
        width: 5px;
        height: 50px;
        background-color: $background-3;
    }

    .okler-themes {
        color: $text-4;
        font-size: $medium-fs;
        cursor: pointer;
    }

    .select {
        color: $text-4;
    }

    .numbered-pages {
        border: 1px solid grey;
    }

    .arrow-icon {
        font-size: $minor-fs;
    }

    .icon, .one, .two {
        border-right: 1px solid grey;
    }

    .icon-2 {
        border-left: 1px solid grey;
    }


</style>