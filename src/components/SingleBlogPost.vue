<template>

        <li class="list-unstyled">
            <span>{{dateNumber}}</span>
            <span>{{dateMonth}}</span>

            <img class="img-fluid" :src="require(`@/assets/${image}.jpg`)" :alt="title">

            <a class="h3 text-decoration-none" :href="url">
                {{title}}
            </a>

            <p>
                {{description}}
            </p>

        <div class="blog-footer d-flex align-items-center">

            <i class="far fa-user"></i>
                <span class="post-data">By {{author}}</span>
            <i class="far fa-folder"></i>
                <span class="post-data">{{category}}</span>
            <i class="far fa-comments"></i>
                <span class="post-data">{{comments}}</span>

            <button class="rounded text-uppercase px-2">
                Read More
            </button>

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
    }

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';

a {
    color: $text-9;
    font-weight: $strong-fw;
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


</style>