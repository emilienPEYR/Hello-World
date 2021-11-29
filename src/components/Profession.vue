<template>
  <div>
    <label for="message">{{ msg }}</label>
  </div>
  <div>
    <select>
      <option value="">--Please choose an option--</option>
      <option value="dog">Bac + 1</option>
      <option value="cat">Bac + 2</option>
      <option value="hamster">Bac + 3</option>
      <option value="parrot">Bac + 4</option>
      <option value="spider">Bac + 5</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Competences",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
</style>