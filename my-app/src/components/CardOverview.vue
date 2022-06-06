<template>
    <div class="row">
        <div class="col-12 col-lg-4" v-for="index in 5" v-bind:key="index">
            <cardApp :cardItem="index" />
        </div>
    </div>
</template>

<script>
    import CardApp from "./CardApp.vue";

    export default {
        name: 'CardOverviewApp',
        components: {
            CardApp,
        },
        props: {
            'cards': Array,
        }
    }
</script>
