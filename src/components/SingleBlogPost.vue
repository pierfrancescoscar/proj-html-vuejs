<template>

        <li class="list-unstyled">
            <span>{{dateNumber}}</span>
            <span>{{dateMonth}}</span>

            <img class="img-fluid" :src="require(`@/assets/${image}.jpg`)" :alt="title">

            <a class="text-decoration-none" :href="url">
                {{title}}
            </a>

            <p>
                {{description}}
            </p>

            <span>{{author}}</span>
            <span>{{category}}</span>
            <span>{{comments}}</span>
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

</style>