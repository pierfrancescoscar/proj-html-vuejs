<template>

<li class="list-unstyled mb-5">
            
            <!-- Normal Single Blog Post Photos -->
            <img v-if="multipleImages == null" class="img-fluid" :src="require(`@/assets/${image}.jpg`)" :alt="title">

            <!-- Last Blog Post with Multiple Photos -->
            <div class="d-flex flex-wrap" v-else>

                <div class="multiple-blog-photos"
                v-for="(element, index) in multipleImages" :key="`image-${index}`">

                    <img class="img-fluid" :src="require(`@/assets/${element}.jpg`)" :alt="title">

                </div>

            </div>

    <div class="blog-main-content pt-3 d-flex">

            <div class="post-date d-flex flex-column text-center pe-3">
                <span class="date-number py-3 px-2">{{dateNumber}}</span>
                <span class="date-month py-1 px-2 text-uppercase">{{dateMonth}}</span>
            </div>

        <div class="blog-content">
                    <div class="heading-blog">
                        <a class="text-decoration-none" href="#">
                            {{title}}
                        </a>

                        <p class="pt-3">
                            {{description}}
                        </p>
                    </div>

                <div class="blog-footer d-flex align-items-center pb-3">

                    <div class="blog-footer-data flex-grow-1 align-items-center">

                        <i class="far fa-user pe-2"></i>
                            <span class="post-data pe-2">By {{author}}</span>
                        <i class="far fa-folder pe-2"></i>
                            <span class="post-data pe-2">{{category}}</span>
                        <i class="far fa-comments pe-2"></i>
                            <span class="post-data pe-2">{{comments}}</span>

                    </div>

                    <div class="blog-cta">

                        <button class="rounded text-uppercase px-2">
                            Read More
                        </button>

                    </div>

                </div>
        </div>

    </div>

</li>
  
</template>

<script>
export default {
    name: 'SingleBlogPost',
    props: {
        image: String,
        title: String,
        description: String,
        dateNumber: String,
        dateMonth: String,
        author: String,
        category: String,
        comments: String,
        multipleImages: Array,
    }

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';
@import '@/style/globals.scss';


a {
    color: $text-9;
    font-weight: $strong-fw;
    font-size: $big-fs;
}

p {
    font-size: $medium-fs;
    color: $text-5;
}

i {
    color: $text-5;
}

button {
    border: 1px solid $text-5;
    background: transparent;
    font-size: $minor-fs;
    color: $text-5;
    font-weight: $light-fw;
}

.post-data {
    font-size: $minor-fs;
    color: $text-4;
}

.blog-footer {
    border-bottom: 1px solid $border-11;
}
    span {
        cursor: pointer;
    }

.date-number {
    background-color: $background-2;
    color: $text-9;
    font-size: $medium-fs;
    font-weight: $strong-fw;
}

.date-month {
    background-color: $background-7;
    color: $text-1;
    font-size: $minor-fs;
    font-weight: $strong-fw;
}

.multiple-blog-photos {
    width: calc(100% / 3);
}

</style>