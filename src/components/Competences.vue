<template>
<div><label for="message">{{ msg }}</label></div>
<div>
  Marketing<input type="checkbox" v-model="message" /><br>
  Design<input type="checkbox" v-model="message" /><br>
  Communication<input type="checkbox" v-model="message" /><br>
  Developpeur<input type="checkbox" v-model="message" /><br>
</div>
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