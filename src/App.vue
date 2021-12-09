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

    <main>
      <!-- Main Articles -->
      <MainArticles :articles="mainPosts" />
      <!-- Popular, Featured Post List -->
      <PostList :popular="popularLinks" />
    </main>
  </div>
</template>

<script>
import TopHeader from '@/components/TopHeader.vue';
import HeaderLogo from '@/components/HeaderLogo.vue';
import Header from '@/components/Header.vue';
import MainArticles from '@/components/MainArticles.vue';
import PostList from '@/components/PostList.vue';


export default {
  name: 'App',
  components: {
    TopHeader,
    HeaderLogo,
    Header,
    MainArticles,
    PostList,
    
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
            ],

            mainPosts: [
                {
                    image: 'blog-46',
                    text: 'How To Take Better Concert Pictures in 30 Seconds',
                    category: 'Photography',
                    url: '/',
                },

                {
                    image: 'blog-47',
                    text: 'Gadget That Make Your Smartphone Even Smarter',
                    category: 'Gadgets',
                    url: '/',
                },

                {
                    image: 'blog-48',
                    text: '20 Top-Rated Tourist Attractions in Manhattan',
                    category: 'Travel',
                    url: '/',
                },

                {
                    image: 'blog-49',
                    text: 'The Best Way To Ride a Motorcycle',
                    category: 'Lifestyle',
                    url: '/',
                },

                {
                    image: 'blog-50',
                    text: '5 Fun Things to Do at the Beach',
                    category: 'Travel',
                    url: '/',
                },

                {
                    image: 'blog-51',
                    text: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
                    category: 'Recipies',
                    url: '/',
                },
            ],

            popularLinks: [
               {
                    image: 'blog-55',
                    text: 'Simple Way to Have a Pretty Face',
                    date: 'January 12, 2019',
                    url: '/',
                },
               {
                    image: 'blog-56',
                    text: 'Ranking the Greatest Players in Basketball',
                    date: 'January 12, 2019',
                    url: '/',
                },
               {
                    image: 'blog-57',
                    text: '4 Ways to Look Cool in Glasses',
                    date: 'January 12, 2019',
                    url: '/',
                },
               {
                    image: 'blog-58',
                    text: 'Tom Camper Trailer Towing Tips',
                    date: 'January 12, 2019',
                    url: '/',
                },
               {
                    image: 'blog-59',
                    text: '5 Lovely Walks in New York',
                    date: 'January 12, 2019',
                    url: '/',
                },
            ],

            
        }
    }
}
</script>

<style lang="scss">
@import '@/style/globals.scss';
@import '@/style/vars.scss';

</style>
