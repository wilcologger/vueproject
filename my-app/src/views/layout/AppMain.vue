<template>
    <main class="main">
        <CardOverviewApp />
    </main>
</template>

<script>
    import CardOverviewApp from '@/components/CardOverview.vue';

    export default {
        name: 'AppMain',
        components: {
            CardOverviewApp,
        }
    }
</script>
