<template>
  <HeaderApp />
  <main>
    <div class="container">
      <router-view></router-view>
    </div>
  </main>
  <FooterApp />
</template>

<script>

import HeaderApp from './components/HeaderApp.vue';
import FooterApp from './components/FooterApp.vue';
export default {
  name: 'App',
  components: {
    HeaderApp,
    FooterApp
  }

}

</script>

<style lang="scss" scoped></style>