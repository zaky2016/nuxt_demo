<template>
  <div class="container">
    <NavBar/>
    <nuxt />
  </div>
</template>

<script>
import NavBar from "../components/navbar";

export default {
  components: { 
      NavBar
       }
};
</script>

<style>
body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1rem;
    line-height: 1.6;
    background: #f4f4f4;
}

.container {
    max-width: 800px;
    margin: 2rem auto;
    overflow: hidden;
    padding: 1rem 2rem;
    background: #FFFF;
}
</style>