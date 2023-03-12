<template>
  <h2>Volume Tracker (0-20)</h2>
  <h2>Current Volume : {{ volume }}</h2>
  <div>
    <button @:click="volume += 2">Increase</button>
    <button @:click="volume -= 2">Decrease</button>
  </div>
  <br />
  <input type="text" v-model="books" />
  <input type="text" v-model="bookInfo.title" />
  <input type="text" v-model="bookInfo.author" />
  <div>
    <button @:click="bookList.push('Ongkar')">Add Book</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      volume: 0,
      books: "The Vinchi Code",
      bookInfo: {
        title: "",
        author: "",
      },
      bookList: ["Satkahon", "Durbeen"],
    };
  },
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert(
          "Listening to a high volume for a long time may damage your hearing."
        );
      }
    },
    books: {
      handler(newValue) {
        console.log(`Calling API with book name = ${newValue}`);
      },
      immediate: true,
    },
    bookInfo: {
      handler(newValue) {
        console.log(
          `Calling API with book title= ${newValue.title} and book author = ${newValue.author}`
        );
      },
      deep: true,
    },
    bookList: {
      handler(newValue) {
        console.log(`Updated Book List ${newValue}`);
      },
      deep: true,
    },
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
