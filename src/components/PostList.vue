<template>
    <section class="container-fluid p-5">
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <h3 class="text-uppercase">Popular Posts</h3>
                    <nav>
                        <ul class="ps-0">
                            <li class="list-unstyled d-flex mb-3 mt-3" v-for="(link, index) in popular" :key="`article-${index}`">

                                <img class="img-fluid me-3 mb-3" :src="require(`@/assets/${link.image}.jpg`)" :alt="link.text">

                                <div class="link-content">

                                    <div class="link-title">
                                        <a class="text-decoration-none" :href="link.url">{{link.text}}</a>
                                    </div>

                                    <div class="link-date">
                                        <span>{{link.date}}</span>
                                    </div>

                                </div>
                            </li>
                        </ul>
                    </nav>
                </div>
                <div class="col-4">
                    <h3 class="text-uppercase">Recent Posts</h3>
                </div>
                <div class="col-4">
                    <h3 class="text-uppercase">Featured Posts</h3>
                </div>
            </div>
        </div>
    </section>
  
</template>

<script>
export default {
    name: 'PostList',
    props: {
        popular: Array,
        recent: Array,
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

    li {
        border-bottom: 1px dashed $text-3;
    }

    img {
        width: 50px;
    }

    a {
        font-size: $medium-fs;
        color: $text-9;
    }

    span  {
        font-size: $minor-fs;
        color: $text-3;
    }

</style>