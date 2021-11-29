<template>
  <h1>Tableau de Prénom</h1>
  <ul>
    <li v-for="item in items" :key="item.message">
      {{ item.message }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      items: [
        { message: "Emilien PEYROT" },
        { message: "Noam SAOUDI" },
        { message: "Souri CHILL" },
        { message: "Romain GRUAT" },
        { message: "Antho FRET" },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
