<template>
    <div class="row">
        <AppCard v-for="(card, index) in cardContent" :cardContent="card" :key="index" />
    </div>
</template>

<script>
    import AppCard from "./AppCard.vue";

    export default {
        name: 'AppCardOverview',
        components: {
            AppCard,
        },
        data() {
            return {
                cardContent: [
                    { title: 'Card title 1', text: 'Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen.'},
                    { title: 'Card title 2', text: 'Vestibulum non pharetra tellus, id tincidunt dui. Pellentesque pharetra nec nisi sit amet sagittis. Nullam pulvinar tortor sit amet augue mollis mollis.'},
                    { title: 'Card title 3', text: 'Cras et cursus enim. Integer rutrum odio non ligula dignissim faucibus. Phasellus blandit porta dictum. Aenean dapibus laoreet odio ut bibendum. Etiam tristique lacus consequat ipsum volutpat mattis. Aenean id quam rutrum, malesuada sapien vel, aliquet ante.'},
                    { title: 'Card title 4', text: 'Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen.'},
                    { title: 'Card title 5', text: 'Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen.'},
                ]
            }
        }
    }
</script>
