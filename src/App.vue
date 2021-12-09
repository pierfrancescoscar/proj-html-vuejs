<template>
  <div id="app">
    <header>
    <!-- Blue Top Header Navigation -->
      <TopHeader :navLink="menuLink" />
    <!-- Logo -->
      <HeaderLogo />
    <!-- Main Navigation -->
      <Header :mainNavigation="mainNavigation" />
    </header>
  </div>
</template>

<script>
import TopHeader from '@/components/TopHeader.vue';
import HeaderLogo from '@/components/HeaderLogo.vue';
import Header from '@/components/Header.vue';


export default {
  name: 'App',
  components: {
    TopHeader,
    HeaderLogo,
    Header,
    
  },
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
            ],

            mainNavigation: [
              {
                    text: 'Home',
                    url: '/',
                },

                {
                    text: 'Elements',
                    url: '/',
                },

                {
                    text: 'Features',
                    url: '/',
                    
                },

                {
                    text: 'Pages',
                    url: '/',
                    
                },

                {
                    text: 'Portfolio',
                    url: '/',
                    
                },

                {
                    text: 'Blog',
                    url: '/',
                    
                },

                {
                    text: 'Shop',
                    url: '/',
                    
                },
            ]

            
        }
    }
}
</script>

<style lang="scss">
@import '@/style/globals.scss';
@import '@/style/vars.scss';

</style>
