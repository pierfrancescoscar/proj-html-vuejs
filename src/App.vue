<template>
  <div id="app">
    <TopHeader />
  </div>
</template>

<script>
import TopHeader from '@/components/TopHeader.vue';


export default {
  name: 'App',
  components: {
    TopHeader,
    
  }
}
</script>

<style lang="scss">
@import '@/style/globals.scss';
@import '@/style/vars.scss';

</style>
