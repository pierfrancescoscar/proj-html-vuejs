<template>
    <section class="top-header container-fluid p-3">
        <div class="container">
            <div class="row">
                <div class="col-12 d-flex align-items-center">
                    <!-- Left - Claim -->
                    <span>
                        Everything about Lifestyle, Travel and Gadgets!
                    </span>
                    <!-- Right - Navigation  -->
                    <nav>
                        <ul class="d-flex align-items-center mb-0">
                            <li class="list-unstyled" v-for="(link, index) in menuLink" :key="`link-${index}`">
                                <a class="text-uppercase text-decoration-none me-4" :href="link.url">{{link.text}}</a>
                            </li>
                        </ul>
                    </nav>


                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'TopHeader',
    data() {
        return {
            menuLink: [
                {
                    text: 'Sign in',
                    url: '/',
                },

                {
                    text: 'About us',
                    url: '/',
                },

                {
                    text: 'Contact us',
                    url: '/',
                    
                },

                {
                    text: 'Buy now',
                    url: '/',
                    
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';

.top-header {
    background-color: $background-4;
}
    span {
        color: $text-1;
        font-size: $minor-fs;
    }

    a {
        color: $text-1;
        font-size: $medium-fs;
        font-weight: $medium-fw;
    }

</style>