<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Toggle />
  <br />
  <br />
  <button v-on:click="step = 'exo2'">Passer à l'exercice 2</button>
  <button v-on:click="step = 'step1'">Commencer un nouveau Formulaire</button>
  <div v-if="step === 'step1'">
    <h1 :style="{ color: colorie }">Formulaire</h1>
    <TextInput msg="Prénom" />
    <TextInput msg="Nom" />
    <br />
    <Calendar />
    <br />
    <Description msg="Message" />
    <br />
    <Profession msg="Profession" />
    <br />
    <Sexe msg="Sexe" />
    <br />
    <Competences msg="Compétences :" />
    <br />
    <Validation msg="" v-on:validation="step = 'step2'" />
  </div>
  <div v-if="step === 'step2'">
    <h1>
      Vous êtes un robot ? <br />
      Si c'est le cas, cliquez sur le bouton "je suis un robot" sinon continuez
    </h1>
    <button v-on:click="step = 'steprobot'">Je suis un robot</button> <br />
    <button v-on:click="step = 'step3'">Continuez !</button>
  </div>
  <div v-if="step === 'steprobot'">
    <h1>Vous n'êtes pas le bienvenue sur ce site</h1>
  </div>
  <div v-if="step === 'step3'">
    <h1>Ton formulaire est bien envoyé</h1>
  </div>
  <div v-if="step === 'exo2'">
    <Exo v-on:enlarge-text="postFontSize += 0.1" @update-cart="updateCart" />
  </div>
</template>

<script>
import Calendar from "./components/Calendar.vue";
import TextInput from "./components/TextInput.vue";
import Toggle from "./components/Toggle.vue";
import Description from "./components/Description.vue";
import Profession from "./components/Profession.vue";
import Sexe from "./components/Sexe.vue";
import Competences from "./components/Competences.vue";
import Validation from "./components/Validation.vue";
import Exo from "./components/Exo.vue";

export default {
  name: "App",
  components: {
    Toggle,
    TextInput,
    Calendar,
    Description,
    Profession,
    Sexe,
    Competences,
    Validation,
    Exo,
  },
  data() {
    return {
      colorie: "red",
      step: "step0",
      postFontSize: 1,
    };
  },
  methods: {
    updateCart(toto) {
      console.log("mettre à jour panier");
      console.log(toto);
    },
    emptyCart() {
      console.log("vider mon panier");
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
