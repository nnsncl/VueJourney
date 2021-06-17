<template>
  <section>
    <!-- <Navigation /> -->
    <!-- <Heading /> -->
    <!-- <form class="form" @submit.prevent='addRecipe' >
      <fieldset class="fieldset">
        <label class="fieldset--label" for='name-field'>Name</label>
        <input class='fieldset--input' name='name-field' v-model='recipe.name' type="text" />
      </fieldset>
      <fieldset class="fieldset">
        <label class="fieldset--label " for="ingredients-field">Ingredients</label>
        <textarea class='fieldset--input' name='ingredients-field' v-model='recipe.ingredients' ></textarea>
      </fieldset>
      <fieldset class="fieldset">
       <label class="fieldset--label " for="steps-field">Steps</label>
        <textarea class='fieldset--input' name='steps-field' v-model='recipe.steps' ></textarea>
      </fieldset>
      <button class='action' type='submit' >Add recipe</button>
    </form>
      <section class="section" v-for="(recipe, index) of recipes" :key='recipe.id' >
        <h1 class="section--title" >{{ recipe.name }}</h1>
        <h3 class="section--subtitle" >Ingredients</h3>
        <div class="flex-container">
          <p class="section--details" >{{ recipe.ingredients }}</p>
        </div>
        <h3 class="section--subtitle" >Steps</h3>
        <div class="flex-container">
          <p class="section--details" >{{ recipe.steps }}</p>
        </div>
        <button class="action" @click='deleteRecipe(index)' >Delete</button>
      </section> -->
      <!-- <section class="section" >
        <ProfilCard
          :pro='true'
          :skills="['Pet Lama', 'Chase Lama', 'Eat Lama']"
          job='Lamas Hunter'
          name='Niki Nik'
          town='Bratislava'
         />
      </section> -->
      
      <section class="section flex-center" >
        <Counter
          v-for="(countItem, index) in counterList"
          :key='index'
          :initCountValue='countItem'
        />
      </section>

  </section>
</template>

<script>
// import {v4 as uuidv4} from 'uuid';

// import Navigation from './components/Navigation.vue'
// import Heading from './components/Heading.vue'
// import ProfilCard from './components/ProfilCard.vue'
import Counter from './components/Counter.vue'

export default {
  name: 'App',
  components: {
    // Navigation,
    // Heading,
    // ProfilCard,
    Counter
  },
data() {
    return {
      counterList: [0, 0, 20, 0, 40, 65]
    }
  },
// data() {
//     return {
//       recipe: {
//         name: "",
//         ingredients: "",
//         steps: "",
//       },
//       recipes: [],
//     };
//   },
  // computed: {
  //   formValid() {
  //     const { name, ingredients, steps } = this.recipe;
  //     return name && ingredients && steps;
  //   },
  // },
  // methods: {
  //   addRecipe() {
  //     if (!this.formValid) {
  //       return;
  //     }
  //     this.recipes.push({
  //       id: uuidv4(),
  //       ...this.recipe,
  //     });
  //   },
  //   deleteRecipe(index) {
  //     this.recipes.splice(index, 1);
  //   },
  // },
};
</script>

<style>
  html, body {
    font-family: Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 62.5%;
    color: #111;
    background: #fafafa;
    max-width: 789px;
    margin: 0 auto;
    padding: 0 2.3rem;
  }
  .form {
    display: flex;
    flex-direction: column;
    gap: 2.3rem;
    margin-bottom: 5.6rem;
  }
  .fieldset {
    all: unset;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }
  .fieldset--label {
    font-size: 1.6rem;
    font-weight: bolder;
  }
  .fieldset--input {
    border-radius: 0.6rem;
    padding: 1.3rem;
    border: 2px solid #D8D8D8;
  }
  .section {
    display: flex;
    flex-direction: column;
    gap: 1.6rem;
    margin-bottom: 3.6rem;
  }
  .section--title {
    font-size: 3.6rem;
    margin: 0;
  }
  .section--subtitle {
    font-size: 2.3rem;
    margin: 0;
  }
  .section--details {
    font-size: 1.6rem;
    color: grey;
  }
  .action {
    all: unset;
    cursor: pointer;
    padding: 1.3rem 2.3rem;
    font-size: 1.3rem;
    background: #111;
    color: white;
    border-radius: 0.5rem;
  }
  .flex-container {
    display: flex;
    flex-direction: column;
  }

  .flex-center {
    padding: 2.3rem 0;
    width: 100%;
    min-height: 80vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
