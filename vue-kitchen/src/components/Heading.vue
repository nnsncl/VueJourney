<template>
  <header class="headding">
        <h1 class="heading--title" >VueJS Journey</h1>
  </header>
</template>

<script>
export default {
  name: 'Heading',
  props: {}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .headding {
        padding: 2.3rem 0;
        text-align: center;
    }

    .heading--title {
        font-size: 5.6rem;
        font-weight: bolder;
        letter-spacing: -0.09rem;
    }

</style>
