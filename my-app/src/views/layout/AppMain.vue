<template>
    <main class="main">
        <AppHero />
        <AppCardOverview />
    </main>
</template>

<script>
import AppHero from '@/components/AppHero.vue'
import AppCardOverview from '@/components/AppCardOverview.vue'

export default {
  name: 'AppMain',
  components: {
    AppHero,
    AppCardOverview
  }
}
</script>
