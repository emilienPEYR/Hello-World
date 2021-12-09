<template>
  <div id="all"> 
    <div>
      <h1>Crypto tracker</h1>
    </div>
    <div class="autocomplete">
      <input
        placeholder="Search"
        v-model="search"
        @input="onChange"
        type="text"
      />
      <ul v-show="isOpen" class="autocomplete-results">
        <li v-for="(result, i) in results" :key="i" class="autocomplete-result">
          {{ result }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Recherche",
  props: {
    items: {
      type: Array,
    },
  },
  data() {
    return {
      results: [],
    };
  },
  methods: {
    filterResults() {
      this.results = this.items.filter(
        (item) => item.toLowerCase().indexOf(this.search.toLowerCase()) > -1
      );
    },
    onChange() {
      this.filterResults();
      this.isOpen = true;
    },
  },
};
</script>

<style>
input {
  padding-left: 16px;
  width: 300px;
  height: 50px;
  border: 1px solid #fff;
  border-radius: 10px;
  margin-bottom: 1em;
}
input:focus {
  border: none;
}
#all {
  background-color: rgb(34, 34, 34);
  color: white;
  padding: 1em;
}
.autocomplete {
  position: relative;
}

.autocomplete-results {
  padding: 0;
  margin: 20em;
  overflow: auto;
  margin-top: 1em;
  margin-bottom: 1em;
}

.autocomplete-result {
  list-style: none;
  text-align: left;
  padding: 4px 2px;
  border-bottom: 1px solid #eeeeee;
  margin: 1em;
  padding: 1em;
}
</style>