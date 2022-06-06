<template>
    <main class="main">
        <div class="content-wrapper">
            <CardOverviewApp />
        </div>
    </main>
</template>

<script>
    import CardOverviewApp from '@/components/CardOverview.vue';

    export default {
        name: 'MainApp',
        components: {
            CardOverviewApp,
        }
    }
</script>
