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
      <PostList :popular="popularLinks" :recent="recentLinks" />
      <!-- Categories Blue Bar -->
      <Categories :categories="categories" />
      <!-- All Blog Post List -->
      <BlogPost :blogPost="blogPost" :instaPost="instagramPhotos" :instaTags="instaTags" />
    </main>

    <footer>
        <Footer :recentPosts="recentFooterPosts" />
    </footer>
  </div>
</template>

<script>
import TopHeader from '@/components/TopHeader.vue';
import HeaderLogo from '@/components/HeaderLogo.vue';
import Header from '@/components/Header.vue';
import MainArticles from '@/components/MainArticles.vue';
import PostList from '@/components/PostList.vue';
import Categories from '@/components/Categories.vue';
import BlogPost from '@/components/BlogPost.vue';
import Footer from '@/components/Footer.vue';



export default {
  name: 'App',
  components: {
    TopHeader,
    HeaderLogo,
    Header,
    MainArticles,
    PostList,
    Categories,
    BlogPost,
    Footer,
    
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

            recentLinks: [
               {
                    image: 'blog-65',
                    text: 'Main Reasons to Stop Text and Driving',
                    date: 'January 12, 2019',
                    url: '/',
                },
               {
                    image: 'blog-66',
                    text: 'Tips To Help You Quickly Prepare your Lunch',
                    date: 'January 12, 2019',
                    url: '/',
                },
               {
                    image: 'blog-67',
                    text: 'Why Should I Buy a Smartwatch?',
                    date: 'January 12, 2019',
                    url: '/',
                },
               {
                    image: 'blog-68',
                    text: 'The Best Augmented reality smartglasses',
                    date: 'January 12, 2019',
                    url: '/',
                },
               {
                    image: 'blog-69',
                    text: '12 Healthiest Foods to Eat for Breakfast',
                    date: 'January 12, 2019',
                    url: '/',
                },
            ],

            categories: [
                {
                    text: 'Gadgets',
                    url: '/',
                },

                {
                    text: 'Photography',
                    url: '/',
                },

                {
                    text: 'Lifestyle',
                    url: '/',
                },

                {
                    text: 'Fashion',
                    url: '/',
                },

                {
                    text: 'Recipies',
                    url: '/',
                },

                {
                    text: 'Travel',
                    url: '/',
                },
            ],

            blogPost: [
                {
                    image: 'blog-54',
                    title: 'How To Make Friends as a Grown-Up',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
                    dateNumber: '12',
                    dateMonth: 'Jan',
                    author: 'John Doe',
                    category: 'Lifestyle, Travel',
                    comments: '12 Comments'

                },

                {
                    image: 'blog-55 (1)',
                    title: 'Simple Ways to Have a Pretty Face',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
                    dateNumber: '12',
                    dateMonth: 'Jan',
                    author: 'John Doe',
                    category: 'Photography, Travel',
                    comments: '12 Comments'

                },

                {
                    image: 'blog-56 (1)',
                    title: 'Ranking The Greatest Players in Basketball',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
                    dateNumber: '12',
                    dateMonth: 'Jan',
                    author: 'John Doe',
                    category: 'Sports, Business',
                    comments: '12 Comments'

                },

                {
                    image: 'blog-58 (1)',
                    title: 'Top Camper Trailer Towing Tips',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
                    dateNumber: '12',
                    dateMonth: 'Jan',
                    author: 'John Doe',
                    category: 'Lifestyle, Travel',
                    comments: '12 Comments'

                },

                {
                    multipleImages: ['blog-13', 'blog-16', 'blog-20', 'blog-23', 'blog-29', 'blog-40'],
                    title: '10 Best Travel Tips After 5 Years Traveling the World',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
                    dateNumber: '8',
                    dateMonth: 'Jan',
                    author: 'John Doe',
                    category: 'Travel, Lifestyle',
                    comments: '12 Comments'

                },
                
            ],

            instagramPhotos: [
                '29739607_2020680068220520_4509928046932787200_n', '30087804_253872848488989_8792603541668626432_n',
                '29415620_196477127626244_3250318472361541632_n',
                '30078414_1274410412703843_8290935809419247616_n',
                '30077195_2066750973610181_3733150062893596672_n',
                '29415304_166583630713703_1032667922171953152_n',
            ],

            instaTags: [

                {
                    text: 'Design',
                    url: '/',
                },

                {
                    text: 'Brands',
                    url: '/',
                },

                {
                    text: 'Video',
                    url: '/',
                },

                {
                    text: 'Business',
                    url: '/',
                },

                {
                    text: 'Travel',
                    url: '/',
                },
            ],

            recentFooterPosts: [
                {
                    image: 'our-office-4-square',
                    text: 'Lorem ipsum dolor sit, consectur adiscipling elit.',
                    date: '12:53 AM Dec 19th',
                    url: '/',
                },

                {
                    image: 'our-office-5-square',
                    text: 'Lorem ipsum dolor sit, consectur adiscipling elit.',
                    date: '12:53 AM Dec 19th',
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
