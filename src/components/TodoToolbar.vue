<template>
  <div class="stick">
    <div class="top">
      <h3><span aria-label="Todo app icon"></span></h3>
    </div>
    <div class="search">
      <input
        type="text"
        v-model="searchbar"
        class="searchTerm"
        placeholder="Search here.."
      />

      <button type="submit" onclick="myFunction()" class="searchButton">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5"
          viewBox="0 0 20 20"
          fill="currentColor"
        >
          <path
            fill-rule="evenodd"
            d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
            clip-rule="evenodd"
          />
        </svg>
      </button>
    </div>
    <div class="results">
      <ul class="no-bullets">
        <li class="lii" v-for="(i, index) in searchbar" :key="index">
          {{ repeat(searchbar, index + 1) }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import { ref, reactive, shallowReactive } from "vue";

export default {
  data() {
    return { searchbar: "" };
  },
  methods: {
    repeat: function (string, count) {
      let temp = "";

      for (let i = 0; i < count; i++) {
        temp = temp + string;
      }
      return temp;
    },
  },

  computed: {
    message: function () {
      let arr = [];
      for (let i = 1; i <= this.searchbar.length; ++i) {
        for (let j = 1; j <= i; ++j) {
          arr.push(this.searchbar);
        }
      }

      // let result = arr.reduce((accumulator, current) => {
      //   return accumulator + current + "\n";
      //  }, "");
      //  return result;
      return arr;
    },
  },
};
</script>

<style lang="scss" scoped>
.Toolbar {
  background-color: none;
}
button.response {
  margin-left: 10px;
  background-color: #0b102e;
  color: white;
  border: none;
}

button.resp {
  background-color: #0b102e;
  color: white;
  border: none;
}

input,
button,
select,
textarea {
  padding: 1em;
  margin: 0 0 1em 0;
  box-sizing: border-box;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.demo {
  font-family: sans-serif;
  border: 1px solid #eee;
  border-radius: 2px;
  padding: 20px 30px;
  margin-top: 1em;
  margin-bottom: 40px;
  user-select: none;
  overflow-x: auto;
}
.stick {
  background-color: white;

  top: 0;
}

.status {
  margin-right: 10px;
  display: inline;
}
</style>