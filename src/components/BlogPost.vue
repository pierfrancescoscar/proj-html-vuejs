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
                  Test
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

</style>