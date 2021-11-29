<template>
<div><label for="message">{{ msg }}</label></div>
<div><input type="text" v-model="message" /></div>
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