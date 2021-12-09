<template>
  <div id="app">
    <header>
    <!-- Blue Top Header Navigation -->
      <TopHeader :navLink="menuLink" />
    <!-- Logo -->
      <HeaderLogo />
    </header>
  </div>
</template>

<script>
import TopHeader from '@/components/TopHeader.vue';
import HeaderLogo from '@/components/HeaderLogo.vue';


export default {
  name: 'App',
  components: {
    TopHeader,
    HeaderLogo,
    
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
            ]
        }
    }
}
</script>

<style lang="scss">
@import '@/style/globals.scss';
@import '@/style/vars.scss';

</style>
