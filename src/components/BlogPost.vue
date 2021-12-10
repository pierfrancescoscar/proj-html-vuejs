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

                  <div class="tweets-container d-flex pt-4">

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

    .tweet {
        color: $text-3;
        font-size: $medium-fs;
    }

    .tweet-date {
        color: $text-4;
        font-size: $minor-fs;
    }

</style>