<template>
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>

  <div v-for="writter in writters" :key="writter.name">
    <h2>{{ writter.name }}</h2>
    <h3 v-for="book in writter.books" :key="book">{{ book }}</h3>
  </div>

  <h2 v-for="(value, key, index) in myInfo" :key="value">
    {{ index }} {{ key }} {{ value }}
  </h2>

  <template v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <hr />
  </template>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["Monayem", "Nafi", "Nawsin"],
      fullNames: [
        { first: "Monayem", last: "Islam" },
        { first: "Zobayer", last: "Nafi" },
        { first: "Tasnuva", last: "Nawsin" },
      ],
      writters: [
        {
          name: "Ahmed Sofa",
          books: ["Gavi Bittanto", "Bangali Musolmaner Mon"],
        },
        {
          name: "Somoresh Mojumder",
          books: ["Satkahon", "At kuthuri Noy doroja"],
        },
      ],
      myInfo: {
        name: "Monayem Islam Tamal",
        channel: "Return One",
        Course: "Vue 3",
      },
    };
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
