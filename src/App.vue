<template>
  <div id="app">
    <Header/>
    <main>
      <PageContent/>
      <BrandServices/> 
    </main>
    <Footer/>   
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import PageContent from '@/components/PageContent.vue';
import BrandServices from '@/components/BrandServices.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    PageContent,
    BrandServices,
    Footer
  }
}
</script>

<style lang="scss">
  @import "/assets/style/common";
  @import "/assets/style/common";
</style>
