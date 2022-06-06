<template>
    <div class="col-12 col-lg-4">
        <div class="card mb-4">
            <img src="https://placedog.net/300/280" alt="dog" class="card-img-top">
            <div class="card-body">
                <div class="card-title h3">{{ cardContent.title }}</div>
                <div class="card-text">
                    <p>Ik ben makelaar in koffi, en woon op de Lauriergracht No 37. Het is mijn gewoonte niet, romans te schrijven, of zulke dingen, en het heeft dan ook lang geduurd, voor ik er toe overging een paar riem papier extra te bestellen, en het werk aan te vangen, dat gij, lieve lezer, zoâven in de hand hebt genomen, en dat ge lezen moet als ge makelaar in koffie zijt, of als ge wat anders zijt. Niet alleen dat ik nooit iets schreef wat naar een roman geleek, maar ik houd er zelfs niet van, iets dergelijks te lezen, omdat ik een man van zaken ben.</p>
                </div>
                <button class="btn btn-primary" v-on:click="nextPage">Next page</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CardApp',
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