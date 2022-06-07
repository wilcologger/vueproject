<template>
    <main class="main">
        <AppCardOverview />
    </main>
</template>

<script>
    import AppCardOverview from '@/components/AppCardOverview.vue';

    export default {
        name: 'AppMain',
        components: {
            AppCardOverview,
        }
    }
</script>
