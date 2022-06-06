<template>
    <div class="row">
        <cardApp v-for="index in cardContent" :cardContent="index" :key="index.title" />
    </div>
</template>

<script>
    import CardApp from "./CardApp.vue";

    export default {
        name: 'CardOverviewApp',
        components: {
            CardApp,
        },
        data() {
            return {
                cardContent: [
                    { title: 'Card title 1', text: 'Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen.'},
                    { title: 'Card title 2', text: 'Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen.'},
                    { title: 'Card title 3', text: 'Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen.'},
                    { title: 'Card title 4', text: 'Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen.'},
                    { title: 'Card title 5', text: 'Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen.'},
                ]
            }
        }
    }
</script>
