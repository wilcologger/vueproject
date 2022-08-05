<template>
  <div class="container">
    <AppHeader />
    <router-view />
    <AppMain />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "./views/layout/AppHeader.vue";
import AppMain from "./views/layout/AppMain.vue";
import AppFooter from "./views/layout/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
};
</script>
