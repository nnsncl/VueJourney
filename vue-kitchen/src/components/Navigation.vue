<template>
  <nav class="nav">
        <img alt="Vue logo" height='50' src="../assets/logo.png">
        <button class="nav--action" >Button</button>
  </nav>
</template>

<script>
export default {
  name: 'Navigation',
  props: {}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 2.3rem 0;
        border-bottom: 1px solid #D8D8D8;
    }

    .nav--action {
        all: unset;
        cursor: pointer;
        padding: 1.3rem 2.3rem;
        border-radius: 0.5rem;
        background: #111;
        color: white;
        font-size: 1.3rem;
        font-weight: 500;
    }

</style>
