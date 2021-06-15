<template>
  <div class="avatar" >
    <div class="avatar--container" >
      <img class="avatar--image" src="https://linktopin.com/assets/images/avatars/random-avatar2.jpg" alt="">
      <span class="avatar--badge" ></span>
    </div>
    <p class="avatar--label" >Niki</p>
  </div>
</template>

<script>
export default {
  name: 'Avatar',
  props: {}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .avatar {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.9rem;
  }
  .avatar--container{
    display: flex;
    flex-direction: column;
    align-items: flex-end;
  }
  .avatar--image {
    max-width: 50px;
    border-radius: 100%;
  }
  .avatar--badge {
    display: block;
    width: 1rem;
    height: 1rem;
    background: lightgreen;
    margin: -1rem 0;
    border-radius: 100%;
  }
  .avatar--label {
    font-size: 1.3rem;
    margin: 0;
  }
</style>
