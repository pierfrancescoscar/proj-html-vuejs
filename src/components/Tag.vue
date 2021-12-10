<template>

    <li class="list-unstyled text-center py-2">
        <a class="text-decoration-none text-uppercase" :href="url">
            {{title}}
        </a>
    </li>
    
</template>

<script>
export default {
    name: 'Tag',
    props: {
        title: String,
        url: String,
    }

}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';

ul {
    border: 1px solid red;
}

li {
    background-color: $background-8;
    width: 150px;
    cursor: pointer;
    &:hover {
        outline: 5px solid $border-8;
    }
    
}

a {
    color: $text-1;
    font-weight: $strong-fw;
    font-size: $minor-fs;
}

</style>