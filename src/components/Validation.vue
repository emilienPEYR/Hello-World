<template>
<div><button v-on:click="$emit('validation')">Confirmer</button></div>
<div><button v-on:click="$emit('validation')">Confirmer</button></div>
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