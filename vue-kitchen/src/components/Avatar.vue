<template>
  <div class="avatar" >
    <article class="avatar--container" >
      <img
        class="avatar--image"
        src="https://linktopin.com/assets/images/avatars/random-avatar2.jpg"
        alt="">
      <span class="avatar--badge" ></span>
    </article>
    <p class="avatar--label" >{{ name }}</p>
  </div>
</template>

<script>
export default {
  name: 'Avatar',
  props: {
    name: {
      type: String,
      required: true,
      default: 'Corbo Boi',
      validator: (value) => {
        return value.length >= 3
      }
    },
    badgeColor: String,
    image: String
  }
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
    background: greenyellow;
    border: 2px solid white;
    margin: -1rem 0;
    border-radius: 100%;
  }
  .avatar--label {
    font-size: 1.3rem;
    margin: 0;
  }
</style>
