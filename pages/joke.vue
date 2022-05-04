<template>
  <div>

      <jokecomponent
        v-for="jok in joke"
        :key="jok.id"
        :id="jok.id"
        :joke="jok.joke"
      />

  </div>
</template>

<script>
import axios from "axios";
import jokecomponent from "../components/jokecomponent";

export default {
  components: {
    jokecomponent,
  },
  data() {
    return {
      joke: [],
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };
    try {
      const res = await axios.get("https://icanhazdadjoke.com/search", config);
      console.log(res.data);
      this.joke = res.data.results;
    } catch (error) {
      console.log(error);
    }
  },
};
</script>

<style>
</style>