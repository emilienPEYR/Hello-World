<template>
  <div>
    <div v-if="isShow"><Hello-world/></div>
    <button v-on:click="isShow = !isShow" id="bouton">Afficher ou Masquer le tableau</button>
  </div>
</template>

<script>
import HelloWorld from './HelloWorld.vue';
export default {
  components: { HelloWorld },
  name: "ToggleDiv",
  data: function () {
    return {
      isShow: true,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#bouton {
  color: white;
  border: 0;
  background-color: #40B883;
  padding: 1em;
  cursor: pointer;
}
</style>