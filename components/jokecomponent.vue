<template>
  <div class="joke">
    <nuxt-link :to="'/' + id" style="text-decoration: none;">
      <p :id="id">{{ joke }}</p>
      <hr />
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: "jokecomponent",
  props: ["joke", "id"],
};
</script>

<style>

</style>