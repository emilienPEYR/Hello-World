<template>
  <h1 :style="{ fontSize: postFontSize + 'em', color: selected }">Le titre de mon site</h1>

  <h1 :style="{ color: selected }">Produits dans mon panier</h1>
  <ul>
    <li v-for="item in cart" v-bind:key="{ item }" :style="{ color: selected }">
      {{ item }}
    </li>
  </ul>

  <button v-on:click="$emit('update-cart', cart)">Passer ma commande</button>
  <br />
  <select v-model="selected">
    <option disabled value="">Choisissez</option>
    <option value="green">Vert</option>
    <option value="black">Noir</option>
    <option value="red">Rouge</option>
    <option value="pink">Rose</option>
    <option value="Yellow">Jaune</option>
    <option value="blue">Bleu</option>
  </select>
  <p>The text is {{ selected }}.</p>
</template>

<script>
export default {
  name: "Exo2",
  data() {
    return {
      cart: ["pain", "fromage", "fleurs", "vin"],
      selected: "Black",
    };
  },
  props: {
    msg: String,
  },
};
</script>
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>