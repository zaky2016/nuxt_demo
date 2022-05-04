<template>
  <div>
<!-- {{$route.params.id}} -->
<p>{{j}}</p>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      j: {},
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };
    try {
      const res = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`, config);
      console.log(this.$route.params.id);
      console.log(res);
    this.j = res.data.joke;
    } catch (error) {
      console.log(error);
    }
  },
};
</script>

<style>
</style>