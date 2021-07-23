<template>
  <div class="todo">
    <todo-page />
  </div>
</template>

<script>
import TodoPage from "./pages/TodoPage.vue";

export default {
  components: {
    TodoPage,
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
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #fafafa;
  min-height: 100vh;
  margin: 0 auto;
}

p {
  margin-left: 10px;
}

p:hover {
  background-color: black;
  color: white;
}
ul.no-bullets {
  list-style-type: none; /* Remove bullets */
  padding: 0; /* Remove padding */
  margin: 0; /* Remove margins */
}
.todo {
  min-width: 600px;
  max-width: calc(30% + 10vw);
  border-radius: 4px;
  padding: 1em;
  background: transparent;
}
.searchTerm {
  width: 90%;
  border: 3px solid black;
  border-right: none;
  padding: 5px;
  height: 20px;
  border-radius: 5px 0 0 5px;
  outline: none;
  color: #9dbfaf;
}

.searchTerm:focus {
  color: black;
}
.searchButton {
  height: 20px;
}
.search {
  position: sticky;
  z-index: 8;
  top: 0;
  background-color: aquamarine;
}
.results {
  word-wrap: break-word;
  user-select: none;
  overflow-x: auto;
  background-color: white;
  padding: 20px;
  text-align: left;
}
@media (max-width: 600px) {
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;

    margin-top: 60px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: white;
    min-height: 100vh;
    margin: 0 auto;
  }
  .todo {
    min-width: 300px;
    max-width: calc(30% + 10vw);
    border-radius: 4px;
    padding: 1em;
    background: transparent;
    word-wrap: break-word;
  }
}
.searchTerm {
  width: 90%;
  border: 3px solid black;
  border-right: none;
  padding: 5px;
  height: 20px;
  border-radius: 5px 0 0 5px;
  outline: none;
  color: #9dbfaf;
}

.searchTerm:focus {
  color: black;
}
.searchButton {
  height: 20px;
}
p {
  margin-left: 10px;
}

p:hover {
  background-color: black;
  color: white;
}
ul.no-bullets {
  list-style-type: none; /* Remove bullets */
  padding: 0; /* Remove padding */
  margin: 0; /* Remove margins */
}
.search {
  position: sticky;
  z-index: 8;
  top: 0;
}
.results {
  word-wrap: break-word;
  user-select: none;
  overflow-x: auto;
  background-color: white;
  padding: 20px;
  text-align: left;
}
</style>