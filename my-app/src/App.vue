<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>

  <AppHeader/>
  <AppMain/>
  <AppFooter/>

  <div class="container">
      <router-view></router-view>
  </div>
  
</template>

<script>
import AppHeader from './views/layout/AppHeader.vue'
import AppMain from './views/layout/AppMain.vue'
import AppFooter from './views/layout/AppFooter.vue'
  
export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
}
</script>