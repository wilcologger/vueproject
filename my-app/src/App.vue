<template>
  <div class="content-wrapper bg-light">
    <div class="container">
      <HeaderApp/>
      <MainApp/>
      <FooterApp/>
    </div>
  </div>
</template>

<script>
import HeaderApp from './views/layout/Header.vue'
import MainApp from './views/layout/Main.vue'
import FooterApp from './views/layout/Footer.vue'

export default {
  name: 'App',
  components: {
    HeaderApp,
    MainApp,
    FooterApp,
  },
}
</script>
