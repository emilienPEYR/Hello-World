<template>
<div><label for="message">{{ msg }}</label></div>
<div> Masculin <input type="radio" v-model="message" /> Féminin <input type="radio" v-model="message" /></div>
</template>

<script>
export default {
  name: "Competences",
  props: {
    msg: String
  }, 
};
</script>

<style scoped>

</style>