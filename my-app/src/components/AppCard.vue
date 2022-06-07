<template>
    <div class="col-12 col-lg-4 mb-3">
        <div class="card h-100 mb-4">
            <img src="https://placedog.net/300/280" alt="dog" class="card-img-top">
            <div class="card-body d-flex flex-column align-items-start">
                <div class="card-title h3">{{ cardContent.title }}</div>
                <div class="card-text">
                    <p>{{ cardContent.text }}</p>
                </div>
                <button class="btn btn-primary mt-auto" v-on:click="nextPage">Next page</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppCard',
        props: {
            cardContent: Object
        },
        methods: {
            nextPage: function() {
                console.log("You have click me!");
            }
        }
    }
</script>