<template>
    <div class="card-container">
        <span v-if='pro' class="pro">PRO</span>
        <img class="round" :src='image' alt="user" />
        <h3>{{ name }}</h3>
        <h6>{{ town }}</h6>
        <p>{{ job }}</p>
        <div class="buttons">
            <button class="primary">
                Message
            </button>
            <button class="primary ghost">
                Following
            </button>
        </div>
        <div class="skills">
            <h6>Skills</h6>
            <ul>
                <li v-for="(skill, index) of skills" :key='index' >{{ skill }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProfilCard',
    props: {
        name: {
        type: String,
        default: 'Ricky Park'
        },
        pro: {
            type: Boolean,
            default: true
        },
        image: {
            type: String,
            required: false,
            default: 'https://randomuser.me/api/portraits/women/56.jpg'
        },
        town: {
            type: String,
            default: 'New York'
        },
        job: {
            type: String,
            default: 'Front end developper'
        },
        skills: {
            type: Array,
            default() {
                return ['UI', 'UX', 'HTML','CSS','JavaScript','React','Node']
            },
        },
    },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Montserrat");

h3 {
  margin: 10px 0;
  font-size: 2.6rem;
}

h6 {
  font-size: 1.6rem;
  margin: 5px 0;
  text-transform: uppercase;
}

p {
  font-size: 1.4rem;
  line-height: 21px;
}

.card-container {
  background-color: #231e39;
  border-radius: 5px;
  box-shadow: 0px 10px 20px -10px rgba(0, 0, 0, 0.75);
  color: #b3b8cd;
  padding-top: 30px;
  position: relative;
  width: 350px;
  max-width: 100%;
  text-align: center;
}

.card-container .pro {
  color: #231e39;
  background-color: #febb0b;
  border-radius: 3px;
  font-size: 1.4rem;
  font-weight: bold;
  padding: 3px 7px;
  position: absolute;
  top: 30px;
  left: 30px;
}

.card-container .round {
  border: 1px solid #03bfcb;
  border-radius: 50%;
  padding: 7px;
}

button.primary {
  background-color: #03bfcb;
  border: 1px solid #03bfcb;
  border-radius: 3px;
  color: #231e39;
  font-family: Montserrat, sans-serif;
  font-weight: 500;
  padding: 10px 25px;
}

button.primary.ghost {
  background-color: transparent;
  color: #02899c;
}

.skills {
  background-color: #1f1a36;
  text-align: left;
  padding: 15px;
  margin-top: 30px;
}

.skills ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.skills ul li {
  border: 1px solid #2d2747;
  border-radius: 2px;
  display: inline-block;
  font-size: 1.3rem;
  margin: 0 7px 7px 0;
  padding: 7px;
}

footer {
  background-color: #222;
  color: #fff;
  font-size: 14px;
  bottom: 0;
  position: fixed;
  left: 0;
  right: 0;
  text-align: center;
  z-index: 999;
}

footer p {
  margin: 10px 0;
}

footer i {
  color: red;
}

footer a {
  color: #3c97bf;
  text-decoration: none;
}
</style>
