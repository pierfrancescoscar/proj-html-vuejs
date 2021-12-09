<template>
  <div id="app">
    <header>
    <!-- Blue Top Header Navigation -->
      <TopHeader />
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
    
  }
}
</script>

<style lang="scss">
@import '@/style/globals.scss';
@import '@/style/vars.scss';

</style>
