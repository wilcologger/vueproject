<template>
    <div class="px-4 py-5 my-5 text-center">
        <img class="d-block mx-auto mb-4" src="./../assets/img/bootstrap-logo.svg" alt="" width="72" height="57">
        <h1 class="display-5 fw-bold">{{ HeroTitle }}</h1>
        <div class="col-lg-6 mx-auto">
            <p class="lead mb-4">{{ HeroMessage }}</p>
            <div class="d-grid gap-2 d-sm-flex justify-content-sm-center">
                <button type="button" class="btn btn-primary btn-lg px-4 gap-3">Primary button</button>
                <button type="button" class="btn btn-outline-secondary btn-lg px-4">Secondary</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'AppHero',
  data () {
    return {
      HeroTitle: 'Centered hero',
      HeroMessage: 'Quickly design and customize responsive mobile-first sites with Bootstrap, the world’s most popular front-end open source toolkit, featuring Sass variables and mixins, responsive grid system, extensive prebuilt components, and powerful JavaScript plugins.'
    }
  }
}
</script>
